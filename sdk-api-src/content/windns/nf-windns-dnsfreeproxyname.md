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

# DnsFreeProxyName function


## -description



			
			The 
<b>DnsFreeProxyName</b> function frees memory allocated for the <b>proxyName</b> member of a <a href="https://msdn.microsoft.com/cfe7653f-7e68-4e50-ba67-bd441f837ef8">DNS_PROXY_INFORMATION</a> structure obtained using the 
<a href="https://msdn.microsoft.com/fdc8eb09-e071-4f03-974a-2b11a657ab18">DnsGetProxyInformation</a> function.


## -parameters




### -param proxyName [in, out]

A pointer to the <b>proxyName</b> string to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/9b3c1c20-5516-41de-b00f-b95736ff53f1">DNS Functions</a>
 

 

