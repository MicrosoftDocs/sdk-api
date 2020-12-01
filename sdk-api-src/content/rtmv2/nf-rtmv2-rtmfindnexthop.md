---
UID: NF:rtmv2.RtmFindNextHop
title: RtmFindNextHop function (rtmv2.h)
description: The RtmFindNextHop function finds a specific next hop in a client's next-hop list.
helpviewer_keywords: ["RtmFindNextHop","RtmFindNextHop function [RAS]","_rtmv2ref_rtmfindnexthop","rras.rtmfindnexthop","rtmv2/RtmFindNextHop"]
old-location: rras\rtmfindnexthop.htm
tech.root: RRAS
ms.assetid: 82bf88ad-eb6d-4ea5-98a0-72280e341f83
ms.date: 12/05/2018
ms.keywords: RtmFindNextHop, RtmFindNextHop function [RAS], _rtmv2ref_rtmfindnexthop, rras.rtmfindnexthop, rtmv2/RtmFindNextHop
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmFindNextHop
 - rtmv2/RtmFindNextHop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmFindNextHop
---

# RtmFindNextHop function


## -description

The 
<b>RtmFindNextHop</b> function finds a specific next hop in a client's next-hop list.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopInfo [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure that contains information identifying the next hop to find. Use the <b>NextHopAddress</b> and <b>InterfaceIndex</b> members to identify the next hop to find.

### -param NextHopHandle [out]

If a handle must be returned: On input, <i>NextHopPointer</i> is a pointer to <b>NULL</b>. On output, if the client owns the next hop, <i>NextHopPointer</i> receives a pointer to the next-hop handle; otherwise, <i>NextHopPointer</i> remains unchanged. 




If a handle does not need to be returned: On input, <i>NextHopPointer</i> is <b>NULL</b>.

### -param NextHopPointer [out]

If a pointer must be returned: On input, <i>NextHopPointer</i> is a pointer to <b>NULL</b>. On output, if the client owns the next hop, <i>NextHopPointer</i> receives a pointer to the next-hop; otherwise, <i>NextHopPointer</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>NextHopPointer</i> is <b>NULL</b>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling client does not own this next hop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified next hop was not found.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The <i>NextHopPointer</i> is valid as long as the client has not released <i>NextHopHandle</i>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddnexthop">RtmAddNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeletenexthop">RtmDeleteNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthoppointer">RtmGetNextHopPointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlocknexthop">RtmLockNextHop</a>