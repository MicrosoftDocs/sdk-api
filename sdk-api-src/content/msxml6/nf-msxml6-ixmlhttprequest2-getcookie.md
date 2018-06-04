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

# IXMLHTTPRequest2::GetCookie


## -description


Gets a cookie associated with the specified URL from the HTTP cookie jar.


## -parameters




### -param pwszUrl

A null-terminated string that specifies the URL in the cookie. 


### -param pwszName

A null-terminated string that specifies the name in the cookie.


### -param dwFlags

A set of bit flags that specifies how this method retrieves the cookies. This parameter can be a set values from the <a href="https://msdn.microsoft.com/185a75cb-3901-4850-a987-803da50e14fd">XHR_COOKIE_FLAG</a> enumeration type defined in the <i>Msxml6.h</i> header file. 

 


### -param pcCookies

A count of cookies pointed to by the <i>ppCookies</i> if the call is successful.


### -param ppCookies [out]

A pointer to the cookies associated with the specified <i>pwszUrl</i> and <i>pwszName</i>.


## -returns



Returns <b>S_OK</b> on success; <b>E_FAIL</b> indicates an error.




## -see-also




<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree Function</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/E150B7CA-A881-4CD5-896F-7E3B6770E105">SetCookie Method</a>



<a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE Structure</a>



<a href="https://msdn.microsoft.com/185a75cb-3901-4850-a987-803da50e14fd">XHR_COOKIE_FLAG</a>
 

 

