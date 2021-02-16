---
UID: NS:rtmv2._RTM_NEXTHOP_LIST
title: RTM_NEXTHOP_LIST (rtmv2.h)
description: The RTM_NEXTHOP_LIST structure contains a list of next hops used to determine equal-cost paths in a route.
helpviewer_keywords: ["*PRTM_NEXTHOP_LIST","PRTM_NEXTHOP_LIST","PRTM_NEXTHOP_LIST structure pointer [RAS]","RTM_NEXTHOP_LIST","RTM_NEXTHOP_LIST structure [RAS]","_rtmv2ref_rtm_nexthop_list","rras.rtm_nexthop_list","rtmv2/PRTM_NEXTHOP_LIST","rtmv2/RTM_NEXTHOP_LIST"]
old-location: rras\rtm_nexthop_list.htm
tech.root: RRAS
ms.assetid: f27269e5-ad7e-4426-ac07-cb3a05532579
ms.date: 12/05/2018
ms.keywords: '*PRTM_NEXTHOP_LIST, PRTM_NEXTHOP_LIST, PRTM_NEXTHOP_LIST structure pointer [RAS], RTM_NEXTHOP_LIST, RTM_NEXTHOP_LIST structure [RAS], _rtmv2ref_rtm_nexthop_list, rras.rtm_nexthop_list, rtmv2/PRTM_NEXTHOP_LIST, rtmv2/RTM_NEXTHOP_LIST'
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
req.typenames: RTM_NEXTHOP_LIST, *PRTM_NEXTHOP_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_NEXTHOP_LIST
 - rtmv2/_RTM_NEXTHOP_LIST
 - PRTM_NEXTHOP_LIST
 - rtmv2/PRTM_NEXTHOP_LIST
 - RTM_NEXTHOP_LIST
 - rtmv2/RTM_NEXTHOP_LIST
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
 - RTM_NEXTHOP_LIST
---

# RTM_NEXTHOP_LIST structure


## -description

The 
<b>RTM_NEXTHOP_LIST</b> structure contains a list of next hops used to determine equal-cost paths in a route.

## -struct-fields

### -field NumNextHops

Specifies the number of equal cost next hops in <b>NextHops</b>.

### -field NextHops

Array of next-hop handles.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>