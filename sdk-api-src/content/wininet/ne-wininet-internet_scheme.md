---
UID: NE:wininet.INTERNET_SCHEME
title: INTERNET_SCHEME
author: windows-sdk-content
description: Defines the flags used with the nScheme member of the URL_COMPONENTS structure.
old-location: wininet\internet_scheme_enumerated_type.htm
old-project: wininet
ms.assetid: 640d0b62-a44f-4115-be27-9976da4bc73a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPINTERNET_SCHEME, INTERNET_SCHEME, INTERNET_SCHEME enumeration [WinINet], INTERNET_SCHEME_DEFAULT, INTERNET_SCHEME_FILE, INTERNET_SCHEME_FIRST, INTERNET_SCHEME_FTP, INTERNET_SCHEME_GOPHER, INTERNET_SCHEME_HTTP, INTERNET_SCHEME_HTTPS, INTERNET_SCHEME_JAVASCRIPT, INTERNET_SCHEME_LAST, INTERNET_SCHEME_MAILTO, INTERNET_SCHEME_NEWS, INTERNET_SCHEME_PARTIAL, INTERNET_SCHEME_RES, INTERNET_SCHEME_SOCKS, INTERNET_SCHEME_UNKNOWN, INTERNET_SCHEME_VBSCRIPT, LPINTERNET_SCHEME, LPINTERNET_SCHEME enumeration pointer [WinINet], _inet_internet_scheme_enumerated_type, wininet.internet_scheme_enumerated_type, wininet/ LPINTERNET_SCHEME, wininet/INTERNET_SCHEME, wininet/INTERNET_SCHEME_DEFAULT, wininet/INTERNET_SCHEME_FILE, wininet/INTERNET_SCHEME_FIRST, wininet/INTERNET_SCHEME_FTP, wininet/INTERNET_SCHEME_GOPHER, wininet/INTERNET_SCHEME_HTTP, wininet/INTERNET_SCHEME_HTTPS, wininet/INTERNET_SCHEME_JAVASCRIPT, wininet/INTERNET_SCHEME_LAST, wininet/INTERNET_SCHEME_MAILTO, wininet/INTERNET_SCHEME_NEWS, wininet/INTERNET_SCHEME_PARTIAL, wininet/INTERNET_SCHEME_RES, wininet/INTERNET_SCHEME_SOCKS, wininet/INTERNET_SCHEME_UNKNOWN, wininet/INTERNET_SCHEME_VBSCRIPT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: INTERNET_SCHEME, *LPINTERNET_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_SCHEME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# INTERNET_SCHEME enumeration


## -description


Defines the flags used with the 
<b>nScheme</b> member of the 
<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a> structure.


## -enum-fields




### -field INTERNET_SCHEME_PARTIAL

Partial URL. 


### -field INTERNET_SCHEME_UNKNOWN

Unknown URL scheme. 


### -field INTERNET_SCHEME_DEFAULT

Default URL scheme. 


### -field INTERNET_SCHEME_FTP

FTP URL scheme (ftp:). 


### -field INTERNET_SCHEME_GOPHER

Gopher URL scheme (gopher:). 

<div class="alert"><b>Note</b>  Windows XP and Windows Server 2003 R2 and earlier only.</div>
<div> </div>

### -field INTERNET_SCHEME_HTTP

HTTP URL scheme (http:). 


### -field INTERNET_SCHEME_HTTPS

HTTPS URL scheme (https:). 


### -field INTERNET_SCHEME_FILE

File URL scheme (file:). 


### -field INTERNET_SCHEME_NEWS

News URL scheme (news:). 


### -field INTERNET_SCHEME_MAILTO

Mail URL scheme (mailto:). 


### -field INTERNET_SCHEME_SOCKS

Socks URL scheme (socks:). 


### -field INTERNET_SCHEME_JAVASCRIPT

JScript URL scheme (javascript:). 


### -field INTERNET_SCHEME_VBSCRIPT

VBScript URL scheme (vbscript:). 


### -field INTERNET_SCHEME_RES

Resource URL scheme (res:).


### -field INTERNET_SCHEME_FIRST

Lowest known scheme value. 


### -field INTERNET_SCHEME_LAST

Highest known scheme value. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/faebdd29-f746-486b-b779-cceeecac9163">URL_COMPONENTS</a>
 

 

