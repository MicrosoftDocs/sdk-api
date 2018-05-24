---
UID: NS:rtmv2._RTM_DEST_INFO
title: "_RTM_DEST_INFO"
author: windows-driver-content
description: The RTM_DEST_INFO structure is used to exchange destination information with clients registered with the routing table manager.
old-location: rras\rtm_dest_info.htm
old-project: RRAS
ms.assetid: 6712ed2f-c5b4-416b-b345-a3d0c5d26820
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PRTM_DEST_INFO, PRTM_DEST_INFO, PRTM_DEST_INFO structure pointer [RAS], RTM_DEST_INFO, RTM_DEST_INFO structure [RAS], _RTM_DEST_INFO, _rtmv2ref_rtm_dest_info, rras.rtm_dest_info, rtmv2/PRTM_DEST_INFO, rtmv2/RTM_DEST_INFO"
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
req.typenames: RTM_DEST_INFO, *PRTM_DEST_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_DEST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RTM_DEST_INFO structure


## -description


The 
<b>RTM_DEST_INFO</b> structure is used to exchange destination information with clients registered with the routing table manager.


## -struct-fields




### -field DestHandle

Handle to the destination.


### -field DestAddress

Specifies the destination network address as an address and a mask.


### -field LastChanged

Specifies the last time this destination was updated.


### -field BelongsToViews

Specifies the views to which this destination belongs.


### -field NumberOfViews

Indicates the number of ViewInfo structures present in this destination.


### -field ViewId

 


### -field NumRoutes

 


### -field Route

 


### -field Owner

 


### -field DestFlags

 


### -field HoldRoute

 


### -field ViewInfo

Structure of the following components. 



#### ViewId

Specifies the view to which this information applies. 



#### NumRoutes

Specifies the number of routes in each of the supported views. 



#### Route

Handle to the best route (with matching criteria) in each of the supported views. 



#### Owner

Handle to the owner of the best route in each of the supported views.



#### DestFlags

Specifies the flags for the best route in each of the supported views. 



#### HoldRoute

Handle to the route that is in a hold-down state in each of the supported views. 


## -see-also




<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/2b22927d-a857-4bcb-9d89-6ca156b04ea9">RtmGetChangedDests</a>



<a href="https://msdn.microsoft.com/bf6525ea-5f32-41d3-b436-920e7369b926">RtmGetDestInfo</a>



<a href="https://msdn.microsoft.com/f793b54e-9591-4b9f-b109-8487013c7af5">RtmGetEnumDests</a>



<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a>



<a href="https://msdn.microsoft.com/b6ff1b1f-fd0e-4cfb-9030-67e27e8578f6">RtmGetLessSpecificDestination</a>



<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>



<a href="https://msdn.microsoft.com/43992abd-7e52-4d1b-b693-f437f5ba77cb">RtmReleaseDestInfo</a>



<a href="https://msdn.microsoft.com/eb338b7f-8461-4980-b92f-09d976661ff2">RtmReleaseDests</a>
 

 

