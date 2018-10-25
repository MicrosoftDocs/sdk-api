---
UID: NS:rtmv2._RTM_NEXTHOP_LIST
title: "_RTM_NEXTHOP_LIST"
author: windows-sdk-content
description: The RTM_NEXTHOP_LIST structure contains a list of next hops used to determine equal-cost paths in a route.
old-location: rras\rtm_nexthop_list.htm
tech.root: rras
ms.assetid: f27269e5-ad7e-4426-ac07-cb3a05532579
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PRTM_NEXTHOP_LIST, PRTM_NEXTHOP_LIST, PRTM_NEXTHOP_LIST structure pointer [RAS], RTM_NEXTHOP_LIST, RTM_NEXTHOP_LIST structure [RAS], _RTM_NEXTHOP_LIST, _rtmv2ref_rtm_nexthop_list, rras.rtm_nexthop_list, rtmv2/PRTM_NEXTHOP_LIST, rtmv2/RTM_NEXTHOP_LIST"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_NEXTHOP_LIST
product: Windows
targetos: Windows
req.typenames: RTM_NEXTHOP_LIST, *PRTM_NEXTHOP_LIST
req.redist: 
---

# _RTM_NEXTHOP_LIST structure


## -description


The 
<b>RTM_NEXTHOP_LIST</b> structure contains a list of next hops used to determine equal-cost paths in a route.


## -struct-fields




### -field NumNextHops

Specifies the number of equal cost next hops in <b>NextHops</b>.


### -field NextHops

Array of next-hop handles.


## -see-also




<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>
 

 

