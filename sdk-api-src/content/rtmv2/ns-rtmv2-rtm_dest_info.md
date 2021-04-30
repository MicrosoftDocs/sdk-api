---
UID: NS:rtmv2._RTM_DEST_INFO
title: RTM_DEST_INFO (rtmv2.h)
description: The RTM_DEST_INFO structure is used to exchange destination information with clients registered with the routing table manager.
helpviewer_keywords: ["*PRTM_DEST_INFO","PRTM_DEST_INFO","PRTM_DEST_INFO structure pointer [RAS]","RTM_DEST_INFO","RTM_DEST_INFO structure [RAS]","_rtmv2ref_rtm_dest_info","rras.rtm_dest_info","rtmv2/PRTM_DEST_INFO","rtmv2/RTM_DEST_INFO"]
old-location: rras\rtm_dest_info.htm
tech.root: RRAS
ms.assetid: 6712ed2f-c5b4-416b-b345-a3d0c5d26820
ms.date: 12/05/2018
ms.keywords: '*PRTM_DEST_INFO, PRTM_DEST_INFO, PRTM_DEST_INFO structure pointer [RAS], RTM_DEST_INFO, RTM_DEST_INFO structure [RAS], _rtmv2ref_rtm_dest_info, rras.rtm_dest_info, rtmv2/PRTM_DEST_INFO, rtmv2/RTM_DEST_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTM_DEST_INFO, *PRTM_DEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_DEST_INFO
 - rtmv2/_RTM_DEST_INFO
 - PRTM_DEST_INFO
 - rtmv2/PRTM_DEST_INFO
 - RTM_DEST_INFO
 - rtmv2/RTM_DEST_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_DEST_INFO
---

# RTM_DEST_INFO structure


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

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetdestinfo">RtmGetDestInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlessspecificdestination">RtmGetLessSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedestinfo">RtmReleaseDestInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>