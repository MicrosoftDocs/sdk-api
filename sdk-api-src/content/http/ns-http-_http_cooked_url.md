---
UID: NS:http._HTTP_COOKED_URL
title: "_HTTP_COOKED_URL"
author: windows-sdk-content
description: Contains a validated, canonical, UTF-16 Unicode-encoded URL request string together with pointers into it and element lengths.
old-location: http\http_cooked_url.htm
old-project: http
ms.assetid: beb31444-4a4b-4d8d-b88b-7d74467c9ca1
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_COOKED_URL, HTTP_COOKED_URL, HTTP_COOKED_URL structure [HTTP], PHTTP_COOKED_URL, PHTTP_COOKED_URL structure pointer [HTTP], _HTTP_COOKED_URL, _http_http_cooked_url, http.http_cooked_url, http/HTTP_COOKED_URL, http/PHTTP_COOKED_URL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HTTP_COOKED_URL, *PHTTP_COOKED_URL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_COOKED_URL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_COOKED_URL structure


## -description


The 
<b>HTTP_COOKED_URL</b> structure contains a validated, canonical, UTF-16 Unicode-encoded URL request string together with pointers into it and element lengths. This is the string that the HTTP Server API matches against registered 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix strings</a> in order to route the request appropriately.


## -struct-fields




### -field FullUrlLength

Size, in bytes, of the data pointed to by the <b>pFullUrl</b> member, not including a terminating null character.


### -field HostLength

Size, in bytes, of the data pointed to by the <b>pHost</b> member.


### -field AbsPathLength

Size, in bytes, of the data pointed to by the <b>pAbsPath</b> member.


### -field QueryStringLength

Size, in bytes, of the data pointed to by the <b>pQueryString</b> member.


### -field pFullUrl

Pointer to the scheme element at the beginning of the URL (must be either "http://..." or "https://...").


### -field pHost

Pointer to the first character in the host element, immediately following the double slashes at the end of the scheme element.


### -field pAbsPath

Pointer to the third forward slash ("/") in the string. In a UrlPrefix string, this is the slash immediately preceding the relativeUri element.


### -field pQueryString

Pointer to the first question mark (?) in the string, or <b>NULL</b> if there is none.


## -remarks



For example, if <b>pFullUrl</b> is "http://www.fabrikam.com/path1/path2/file.ext?n1=v1&amp;n2=v2", then <b>pHost</b> points to "www.fabrikam", <b>pAbsPath</b> points to "/path1/…" and <b>pQueryString</b> points to "?n1=v1…".




## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>
 

 

