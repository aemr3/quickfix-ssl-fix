This repository is implements a fix to compile package on OSX. You will
need to install openssl via homebrew before installing this package.
Run following commands to use homebrew's openssl on the compilation step:

```
export LDFLAGS="-L/opt/homebrew/opt/openssl@1.1/lib"
export LDFLAGS="-L/opt/homebrew/opt/openssl@3/lib"
export CPPFLAGS="-I/opt/homebrew/opt/openssl@1.1/include"
export CPPFLAGS="-I/opt/homebrew/opt/openssl@3/include"
```


---

This package is a fork of the Quickfix project that exposes the
SSL capabilities of the library to Python. The pull request can
be found [here](https://github.com/quickfix/quickfix/pull/361).

Differences to the official [quickfix](https://pypi.org/project/quickfix/)
package are:

- The SSLSocketInitiator and SSLSocketAcceptor are now available.
- UtcTimeStamp, UtcDate and UtcTimeOnly are now exposed.
- A getDateTime() method is added to UtcTimeStamp which will return
  a python datetime.
- A setFromString() method is added to SessionSettings
  
## License requirements

The QuickFIX Software License, Version 1.0
 
Copyright (c) 2001-2018 Oren Miller

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
 
2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in
   the documentation and/or other materials provided with the
   distribution.

3. The end-user documentation included with the redistribution,
   if any, must include the following acknowledgment:
      "This product includes software developed by
       quickfixengine.org (http://www.quickfixengine.org/)."
   Alternately, this acknowledgment may appear in the software itself,
   if and wherever such third-party acknowledgments normally appear.
 
4. The names "QuickFIX" and "quickfixengine.org" must
   not be used to endorse or promote products derived from this
   software without prior written permission. For written
   permission, please contact ask@quickfixengine.org
 
5. Products derived from this software may not be called "QuickFIX",
   nor may "QuickFIX" appear in their name, without prior written
   permission of quickfixengine.org
 
THIS SOFTWARE IS PROVIDED ``AS IS'' AND ANY EXPRESSED OR IMPLIED
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES
OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED.  IN NO EVENT SHALL QUICKFIXENGINE.ORG OR
ITS CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF
USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT
OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
SUCH DAMAGE.



