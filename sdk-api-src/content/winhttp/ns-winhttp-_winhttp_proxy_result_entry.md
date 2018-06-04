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

# _WINHTTP_PROXY_RESULT_ENTRY structure


## -description


The <b>WINHTTP_PROXY_RESULT_ENTRY</b> structure contains a result entry from a call to <a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>.


## -struct-fields




### -field fProxy

A <b>BOOL</b> that whether a result is from a proxy. It is set to <b>TRUE</b>   if the result contains a proxy or <b>FALSE</b> if the result does not contain a proxy.


### -field fBypass

A BOOL that indicates if the result is bypassing a proxy (on an intranet). It is set to  <b>TRUE</b> if the result is bypassing a proxy or <b>FALSE</b> if all traffic is direct. This parameter applies only if <i>fProxy</i> is <b>FALSE</b>.


### -field ProxyScheme

An <a href="https://msdn.microsoft.com/31e45879-807e-4dd5-9f99-94a46011e55e">INTERNET_SCHEME</a> value that specifies the scheme of the proxy.


### -field pwszProxy

A string that contains the hostname of the proxy.


### -field ProxyPort

An <a href="https://msdn.microsoft.com/535d644d-4045-4ff1-9c12-a3d5f665453d">INTERNET_PORT</a> value that specifies the port of the proxy.


## -remarks



This structure is stored in an array inside of a <a href="https://msdn.microsoft.com/6a621701-3325-4877-99ba-8580ad07739d">WINHTTP_PROXY_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/6a621701-3325-4877-99ba-8580ad07739d">WINHTTP_PROXY_RESULT</a>



<a href="https://msdn.microsoft.com/0484bf54-066f-4a7f-8d1a-079eb4b001bd">WinHttpFreeProxyResult</a>



<a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>
 

 

