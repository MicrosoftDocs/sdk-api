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

# _WINHTTP_PROXY_RESULT structure


## -description


The <b>WINHTTP_PROXY_RESULT</b> structure contains  collection of proxy result entries provided by <a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>.


## -struct-fields




### -field cEntries

The number of entries in the <b>pEntries</b> array.


### -field pEntries

A pointer to an array of <a href="https://msdn.microsoft.com/d1652b34-67a9-40ad-a495-836147e5cc88">WINHTTP_PROXY_RESULT_ENTRY</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/d1652b34-67a9-40ad-a495-836147e5cc88">WINHTTP_PROXY_RESULT_ENTRY</a>



<a href="https://msdn.microsoft.com/0484bf54-066f-4a7f-8d1a-079eb4b001bd">WinHttpFreeProxyResult</a>



<a href="https://msdn.microsoft.com/f594e588-b3da-4afb-a5f9-552759bca148">WinHttpGetProxyResult</a>
 

 

