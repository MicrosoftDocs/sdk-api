---
UID: NS:http._HTTP_VERSION
title: HTTP_VERSION (http.h)
author: windows-sdk-content
description: Defines a version of the HTTP protocol that a request requires or a response provides.
old-location: http\http_version.htm
tech.root: http
ms.assetid: 8f97410c-27b5-4225-849e-ee55e4c5f762
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_VERSION, HTTP_VERSION, HTTP_VERSION structure [HTTP], PHTTP_VERSION, PHTTP_VERSION structure pointer [HTTP], _http_http_version, http.http_version, http/HTTP_VERSION, http/PHTTP_VERSION"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_VERSION
product: Windows
targetos: Windows
req.typenames: HTTP_VERSION, *PHTTP_VERSION
req.redist: 
---

# HTTP_VERSION structure


## -description


The 
<b>HTTP_VERSION</b> structure defines a version of the HTTP protocol that a request requires or a response provides. This is not to be confused with the version of the HTTP Server API used, which is stored in an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure.


## -struct-fields




### -field MajorVersion

Major version of the HTTP protocol.


### -field MinorVersion

Minor version of the HTTP protocol.


## -remarks



For more information about the HTTP protocol, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84048">RFC 2616</a>.

The following macros define various versions of the HTTP protocol:"#define HTTP_VERSION_UNKNOWN    { 0, 0 }""#define HTTP_VERSION_0_9        { 0, 9 }""#define HTTP_VERSION_1_0        { 1, 0 }""#define HTTP_VERSION_1_1        { 1, 1 }"

The HTTP Server API provides a number of macros that can be used to evaluate the value of an HTTP_VERSION structure; For more information, see 
<a href="https://msdn.microsoft.com/9c5fb0a4-fda8-4489-8a1e-c232079bd501">HTTP Server API Version 1.0 Macros</a>.

<div class="alert"><b>Note</b>  The HTTP Server API rejects a version of HTTP larger than 65,535 in either the major or minor portion. If a request includes such a version number, the HTTP Server API discards it and returns a response with status 400 ("Bad Request").</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>
 

 

