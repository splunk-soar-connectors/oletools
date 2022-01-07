[comment]: # "Auto-generated SOAR connector documentation"
# Oletools

Publisher: Splunk Community  
Connector Version: 1\.0\.2  
Product Vendor: decalage2  
Product Name: oletools  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.9\.39220  

This app provides actions to analyze Microsoft OLE2 files such as Microsoft Office Documents of Outlook messages\. It is based on the oletools toolkit

[comment]: # " File: readme.md"
[comment]: # "  Copyright (c) 2021 Splunk Inc."
[comment]: # ""
[comment]: # "  Licensed under Apache 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)"
[comment]: # ""
## SDK and SDK Licensing details for the app

### oletools

This app uses the oletools module, which is licensed under the BSD License (BSD), Copyright (c)
2012-2021 Philippe Lagadec (http://www.decalage.info).

This license applies to the python-oletools package, apart from the thirdparty folder which contains
third-party files published with their own license.

All rights reserved. Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met: Redistributions of
source code must retain the above copyright notice, this list of conditions and the following
disclaimer. Redistributions in binary form must reproduce the above copyright notice, this list of
conditions and the following disclaimer in the documentation and/or other materials provided with
the distribution. THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH
DAMAGE.

### olevba

olevba contains modified source code from the officeparser project, published under the following
MIT License (MIT):

officeparser is Copyright (c) 2014-2021 John William Davison. Permission is hereby granted, free of
charge, to any person obtaining a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and
to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial
portions of the Software. THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### colorclass

This app uses the colorclass module, which is licensed under the MIT License (MIT), Copyright (c)
2014-2021 Robpol86.

### olefile

This app uses the olefile module, which is licensed under the BSD License (BSD), Copyright (c)
2014-2021 Philippe Lagadec.

  
**Note:** The app is not making any REST call. Therefore, the proxy settings will be ignored.


### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[run mraptor scan](#action-run-mraptor-scan) - Perform a MacroRaptor scan on a file  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'run mraptor scan'
Perform a MacroRaptor scan on a file

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**vault\_id** |  required  | Vault ID of the file to scan | string |  `vault id` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.vault\_id | string |  `vault id` 
action\_result\.data\.\*\.mraptor\.autoexec | string | 
action\_result\.data\.\*\.mraptor\.execute | string | 
action\_result\.data\.\*\.mraptor\.suspicious | string | 
action\_result\.data\.\*\.mraptor\.vba\_code | string | 
action\_result\.data\.\*\.mraptor\.write | string | 
action\_result\.data\.\*\.oleid\.ObjectPool\.value | string | 
action\_result\.data\.\*\.oleid\.container\.value | string | 
action\_result\.data\.\*\.oleid\.encrypted\.value | string | 
action\_result\.data\.\*\.oleid\.ext\_rels\.value | string | 
action\_result\.data\.\*\.oleid\.flash\.value | string | 
action\_result\.data\.\*\.oleid\.ftype\.value | string | 
action\_result\.data\.\*\.oleid\.vba\.value | string | 
action\_result\.data\.\*\.oleid\.xlm\.value | string | 
action\_result\.status | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 