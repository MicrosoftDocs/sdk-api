---
UID: NF:rtmv2.RtmAddNextHop
title: RtmAddNextHop function (rtmv2.h)
description: The RtmAddNextHop function adds a new next-hop entry or updates an existing next-hop entry to a client's next-hop list.
helpviewer_keywords: ["RTM_NEXTHOP_FLAGS_DOWN","RTM_NEXTHOP_FLAGS_REMOTE","RtmAddNextHop","RtmAddNextHop function [RAS]","_rtmv2ref_rtmaddnexthop","rras.rtmaddnexthop","rtmv2/RtmAddNextHop"]
old-location: rras\rtmaddnexthop.htm
tech.root: RRAS
ms.assetid: 7c11397b-f5c9-4a3e-88d8-2f1736f5da13
ms.date: 12/05/2018
ms.keywords: RTM_NEXTHOP_FLAGS_DOWN, RTM_NEXTHOP_FLAGS_REMOTE, RtmAddNextHop, RtmAddNextHop function [RAS], _rtmv2ref_rtmaddnexthop, rras.rtmaddnexthop, rtmv2/RtmAddNextHop
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
 - RtmAddNextHop
 - rtmv2/RtmAddNextHop
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
 - RtmAddNextHop
---

# RtmAddNextHop function


## -description

The 
<b>RtmAddNextHop</b> function adds a new next-hop entry or updates an existing next-hop entry to a client's next-hop list. If a next hop already exists, the routing table manager returns a handle to the next hop. This handle can then be used to specify a next hop to a destination when adding or updating a route.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopInfo [in]

Pointer to a structure that contains information identifying the next hop to add or update. The <b>NextHopOwner</b> and <b>State</b> members are ignored; these members are set by the routing table manager. The <b>Flags</b> member can be one of the following values. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_FLAGS_REMOTE"></a><a id="rtm_nexthop_flags_remote"></a><dl>
<dt><b>RTM_NEXTHOP_FLAGS_REMOTE</b></dt>
</dl>
</td>
<td width="60%">
This next hop points to a remote destination that is not directly reachable. To obtain the complete path, the client must perform a recursive lookup.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_NEXTHOP_FLAGS_DOWN"></a><a id="rtm_nexthop_flags_down"></a><dl>
<dt><b>RTM_NEXTHOP_FLAGS_DOWN</b></dt>
</dl>
</td>
<td width="60%">
This flag is reserved for future use.

</td>
</tr>
</table>

### -param NextHopHandle [in, out]

If the client has a handle (client is updating a next hop): On input, <i>NextHopHandle</i> is a pointer to the next-hop handle. On output, <i>NextHopHandle</i> is unchanged. 




If the client does not have a handle and a handle must be returned (client is adding or updating a next hop): On input, <i>NextHopHandle</i> is a pointer to <b>NULL</b>. On output, <i>NextHopHandle</i> receives a pointer to the next-hop handle. The values in <i>NextHopInfo</i> are used to identify the next hop to update.

If a handle does not need to be returned (client is adding or updating a next hop): On input, <i>NextHopHandle</i> is <b>NULL</b>. The values in <i>NextHopInfo</i> are used to identify the next hop to update.

### -param ChangeFlags [out]

On input, <i>ChangeFlags</i> is a pointer to an <b>RTM_NEXTHOP_CHANGE_FLAGS</b> data type. 




On output, <i>ChangeFlags</i> receives a flag indicating whether a next hop was added or updated. If <i>ChangeFlags</i> is zero, a next hop was updated; if <i>ChangeFlags</i> is <b>RTM_NEXTHOP_CHANGE_NEW</b>, a next hop was added.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

If <i>NextHopHandle</i> points to a non-<b>NULL</b> handle, the next hop specified by the handle is updated. Otherwise, a search is made for the address specified by <i>NextHopInfo</i>. If a next hop is found, it is updated. If no match is found, a new next hop is added.

If a handle was returned, release the handle when it is no longer required by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>.

## -see-also

<a href="/windows/desktop/RRAS/next-hop-flags">Next Hop Flags</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeletenexthop">RtmDeleteNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmfindnexthop">RtmFindNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthoppointer">RtmGetNextHopPointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlocknexthop">RtmLockNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>