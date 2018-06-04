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
 

 

