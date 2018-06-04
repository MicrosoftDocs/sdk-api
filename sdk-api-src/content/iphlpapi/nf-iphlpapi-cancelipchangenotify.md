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

# CancelIPChangeNotify function


## -description


The <b>CancelIPChangeNotify</b> function cancels notification of IPv4 address and route changes previously requested with successful calls to the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a> functions.


## -parameters




### -param notifyOverlapped [in]

A pointer to the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure used in the previous call to <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>  or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a>.


## -remarks



The  
<b>CancelIPChangeNotify</b> function deregisters for a change notification previously requested for IPv4 address or route changes on  a local computer. These requests to register for notification are made  by calling the <a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a> or <a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a> functions.  

The <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure used in the previous call to one of these notification functions is passed to <b>CancelIPChangeNotify</b> function in the <i>notifyOverlapped</i> parameter to deregister for notifications.

The <b>CancelIPChangeNotify</b> can return <b>FALSE</b> if no notification request was found or an invalid <i>notifyOverlapped</i> parameter was passed. 




## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/22ac3b5b-452c-454b-8fbd-47a873675c6c">NotifyAddrChange</a>



<a href="https://msdn.microsoft.com/39f2ec4d-131a-4a0a-9740-0d96aaea2dc7">NotifyRouteChange</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

