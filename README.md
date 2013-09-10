Hebmorph-exist
--------------

EXPath packaging for hebmorph Hebrew morphology analyzer 

This is a distribution of the Hebmorph morph analyzer/Lucene extension, compilable as an EXPath package for
the [eXist native XML database] (http://exist-db.org).

To compile, run `ant` from the root of the clone. The XAR package will be built in the `dist/` directory. 
It can be installed using the normal [installation mechanism] (http://exist-db.org/exist/apps/doc/dashboard.xml#D2.2.4.5) for EXPath packages in eXist.

Once installed, you can reference the hebmorph analyzer from `collection.xconf`:

```xml
<collection xmlns="http://exist-db.org/collection-config/1.0">
    <index>
        <fulltext default="none" attributes="no"/>
        <lucene>
            <!-- reference the hebmorph analyzer: -->
            <analyzer class="org.apache.lucene.analysis.hebrew.MorphAnalyzer"/>
            <!-- inline and text -->
        </lucene>
        <!-- range indexes here -->
    </index>
</collection>
```

It would be better if we had a real Java wrapper for eXist's indexing module.

License and source
------------------

Hebmorph is licensed under the GNU Affero General Public License, version 3. A copy of the license is 
included in this distribution.

These Hebmorph binaries were compiled from the source code at https://github.com/opensiddur/HebMorph .
The git revision SHA is 9298a8c71a62af06cac7a8001066b6387020a6b2

All other code is licensed under the MIT License:

Copyright (c) 2013 Open Siddur Project

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

