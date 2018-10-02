---
UID: NF:msxml6.IXMLHTTPRequest2.GetCookie
title: IXMLHTTPRequest2::GetCookie
author: windows-sdk-content
description: Gets a cookie associated with the specified URL from the HTTP cookie jar.
old-location: ixhr2\ixmlhttprequest2_getcookie.htm
tech.root: ixhr2
ms.assetid: A2A9C54B-92A2-41EA-A741-797BA219BCDA
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCookie, GetCookie method [XMLHttpRequest2], GetCookie method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],GetCookie method, IXMLHTTPRequest2.GetCookie, IXMLHTTPRequest2::GetCookie, ixhr2.ixmlhttprequest2_getcookie, msxml6/IXMLHTTPRequest2::GetCookie
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
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
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.GetCookie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

