---
UID: NS:rtmv2._RTM_ENTITY_INFO
title: "_RTM_ENTITY_INFO"
author: windows-driver-content
description: The RTM_ENTITY_INFO structure is used to exchange client information with the routing table manager.
old-location: rras\rtm_entity_info.htm
old-project: RRAS
ms.assetid: b2a1e6b9-0cac-4316-98a0-ff1d44c5a15a
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PRTM_ENTITY_INFO, PRTM_ENTITY_INFO, PRTM_ENTITY_INFO structure pointer [RAS], RTM_ENTITY_INFO, RTM_ENTITY_INFO structure [RAS], _RTM_ENTITY_INFO, _rtmv2ref_rtm_entity_info, rras.rtm_entity_info, rtmv2/PRTM_ENTITY_INFO, rtmv2/RTM_ENTITY_INFO"
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
req.typenames: RTM_ENTITY_INFO, *PRTM_ENTITY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_ENTITY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RTM_ENTITY_INFO structure


## -description


The 
<b>RTM_ENTITY_INFO</b> structure is used to exchange client information with the routing table manager.


## -struct-fields




### -field RtmInstanceId

Specifies the instance of the routing table manager with which the client registered.


### -field AddressFamily

Specifies the address family to which the client belongs.


### -field EntityId

Specifies the identifier that uniquely identifies a client.


## -see-also




<a href="https://msdn.microsoft.com/6c75fb17-60b9-44cb-a934-430a6de74ee7">RTM_ENTITY_ID</a>



<a href="https://msdn.microsoft.com/6062369c-22c7-48e4-9dd3-91efba22df34">RtmGetEntityInfo</a>



<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>



<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>



<a href="https://msdn.microsoft.com/ea72dde4-2d04-4ceb-b718-3ee96bf70464">RtmReleaseEntityInfo</a>
 

 

