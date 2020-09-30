---
UID: NF:rtmv2.RtmLockNextHop
title: RtmLockNextHop function (rtmv2.h)
description: The RtmLockNextHop function locks or unlocks a next hop. This function should be called by the next hop's owner to lock the next hop before making changes to the next hop. A pointer to the next hop is returned.
helpviewer_keywords: ["RtmLockNextHop","RtmLockNextHop function [RAS]","_rtmv2ref_rtmlocknexthop","rras.rtmlocknexthop","rtmv2/RtmLockNextHop"]
old-location: rras\rtmlocknexthop.htm
tech.root: RRAS
ms.assetid: f5b6d430-a50e-49fc-8274-81bac1300477
ms.date: 12/05/2018
ms.keywords: RtmLockNextHop, RtmLockNextHop function [RAS], _rtmv2ref_rtmlocknexthop, rras.rtmlocknexthop, rtmv2/RtmLockNextHop
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
 - RtmLockNextHop
 - rtmv2/RtmLockNextHop
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
 - RtmLockNextHop
---

# RtmLockNextHop function


## -description

The 
<b>RtmLockNextHop</b> function locks or unlocks a next hop. This function should be called by the next hop's owner to lock the next hop before making changes to the next hop. A pointer to the next hop is returned.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopHandle [in]

Handle to the next hop to lock or unlock.

### -param Exclusive [in]

Specifies whether to lock or unlock the next hop in an exclusive (<b>TRUE</b>) or shared (<b>FALSE</b>) mode.

### -param LockNextHop [in]

Specifies whether to lock or unlock the next hop. Specify <b>TRUE</b> to lock the next hop; specify <b>FALSE</b> to unlock it.

### -param NextHopPointer [out]

On input, <i>NextHopPointer</i> is a pointer to <b>NULL</b>. 




On output, if the client owns the next hop, <i>NextHopPointer</i> receives a pointer to the next-hop; otherwise, <i>NextHopPointer</i> remains unchanged.

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

Clients cannot change the <b>NextHopAddress</b> and <b>InterfaceIndex</b> members of the <a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure; these values are used to uniquely identify a next hop.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddnexthop">RtmAddNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeletenexthop">RtmDeleteNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmfindnexthop">RtmFindNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthoppointer">RtmGetNextHopPointer</a>