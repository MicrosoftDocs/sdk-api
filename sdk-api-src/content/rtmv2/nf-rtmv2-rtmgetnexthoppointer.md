---
UID: NF:rtmv2.RtmGetNextHopPointer
title: RtmGetNextHopPointer function (rtmv2.h)
description: The RtmGetNextHopPointer function obtains a direct pointer to the specified next hop. The pointer allows the next-hop owner direct read access to the routing table manager's RTM_NEXTHOP_INFO structure.
helpviewer_keywords: ["RtmGetNextHopPointer","RtmGetNextHopPointer function [RAS]","_rtmv2ref_rtmgetnexthoppointer","rras.rtmgetnexthoppointer","rtmv2/RtmGetNextHopPointer"]
old-location: rras\rtmgetnexthoppointer.htm
tech.root: RRAS
ms.assetid: 61fa3fa2-1cad-4930-975e-8f5b86ad3b05
ms.date: 12/05/2018
ms.keywords: RtmGetNextHopPointer, RtmGetNextHopPointer function [RAS], _rtmv2ref_rtmgetnexthoppointer, rras.rtmgetnexthoppointer, rtmv2/RtmGetNextHopPointer
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
 - RtmGetNextHopPointer
 - rtmv2/RtmGetNextHopPointer
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
 - RtmGetNextHopPointer
---

# RtmGetNextHopPointer function


## -description

The 
<b>RtmGetNextHopPointer</b> function obtains a direct pointer to the specified next hop. The pointer allows the next-hop owner direct read access to the routing table manager's 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopHandle [in]

Handle to the next hop.

### -param NextHopPointer [out]

If the client is the owner of the next hop, <i>NextHopPointer</i> receives a pointer to the next hop.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

Clients should only use this pointer for read-only access.

When the next hop handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthopinfo">RtmReleaseNextHopInfo</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddnexthop">RtmAddNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeletenexthop">RtmDeleteNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmfindnexthop">RtmFindNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlocknexthop">RtmLockNextHop</a>