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

# _RTM_REGN_PROFILE structure


## -description


The 
<b>RTM_REGN_PROFILE</b> structure contains information returned during the registration process. The information is used for later function calls (such as the maximum number of routes that can be returned by a call to 
<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>).


## -struct-fields




### -field MaxNextHopsInRoute

Specifies the maximum number of equal-cost next hops in a route.


### -field MaxHandlesInEnum

Specifies the maximum number of handles that can be returned in one call to 
<a href="https://msdn.microsoft.com/f793b54e-9591-4b9f-b109-8487013c7af5">RtmGetEnumDests</a>, 
<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>, 
<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>, or 
<a href="https://msdn.microsoft.com/9ee40466-63e9-40c4-82bf-45f819d0ae58">RtmGetListEnumRoutes</a>. The number of handles that can be returned is limited (and configurable) to improve efficiency and performance of the routing table manager.


### -field ViewsSupported

Views supported by this address family.


### -field NumberOfViews

Number of views.


## -see-also




<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>
 

 

