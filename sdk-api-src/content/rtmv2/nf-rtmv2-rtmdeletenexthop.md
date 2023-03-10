---
UID: NF:rtmv2.RtmDeleteNextHop
title: RtmDeleteNextHop function (rtmv2.h)
description: The RtmDeleteNextHop function deletes a next hop from the next-hop list.
helpviewer_keywords: ["RtmDeleteNextHop","RtmDeleteNextHop function [RAS]","_rtmv2ref_rtmdeletenexthop","rras.rtmdeletenexthop","rtmv2/RtmDeleteNextHop"]
old-location: rras\rtmdeletenexthop.htm
tech.root: RRAS
ms.assetid: 708a890e-4dc6-49c7-b857-cdb8504e7f7f
ms.date: 12/05/2018
ms.keywords: RtmDeleteNextHop, RtmDeleteNextHop function [RAS], _rtmv2ref_rtmdeletenexthop, rras.rtmdeletenexthop, rtmv2/RtmDeleteNextHop
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
 - RtmDeleteNextHop
 - rtmv2/RtmDeleteNextHop
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
 - RtmDeleteNextHop
---

# RtmDeleteNextHop function


## -description

The 
<b>RtmDeleteNextHop</b> function deletes a next hop from the next-hop list.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopHandle [in]

Handle to the next hop to delete. This parameter is optional and can be set to <b>NULL</b>; if it is <b>NULL</b>, the values in <i>NextHopInfo</i> are used to identify the next hop to delete.

### -param NextHopInfo [in]

Pointer to a structure that contains information identifying the next hop to delete. This parameter is optional and can be set to <b>NULL</b>; if it is <b>NULL</b>, the handle in <i>NextHopHandle</i> is used to identify the next hop to delete.

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

If a client specifies a <i>NextHopHandle</i>, the client should not subsequently release the handle using 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddnexthop">RtmAddNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmfindnexthop">RtmFindNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthoppointer">RtmGetNextHopPointer</a>