---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

