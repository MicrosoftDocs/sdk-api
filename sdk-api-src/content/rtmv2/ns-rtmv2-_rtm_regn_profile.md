---
UID: NS:rtmv2._RTM_REGN_PROFILE
title: "_RTM_REGN_PROFILE"
author: windows-driver-content
description: The RTM_REGN_PROFILE structure contains information returned during the registration process. The information is used for later function calls (such as the maximum number of routes that can be returned by a call to RtmGetEnumRoutes).
old-location: rras\rtm_regn_profile.htm
old-project: RRAS
ms.assetid: 26644a09-8d49-4c9f-a7cd-5edbf93e83d0
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PRTM_REGN_PROFILE, PRTM_REGN_PROFILE, PRTM_REGN_PROFILE structure pointer [RAS], RTM_REGN_PROFILE, RTM_REGN_PROFILE structure [RAS], _RTM_REGN_PROFILE, _rtmv2ref_rtm_regn_profile, rras.rtm_regn_profile, rtmv2/PRTM_REGN_PROFILE, rtmv2/RTM_REGN_PROFILE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RTM_REGN_PROFILE, *PRTM_REGN_PROFILE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_REGN_PROFILE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

