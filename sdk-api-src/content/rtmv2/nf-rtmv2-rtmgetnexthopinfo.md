---
UID: NF:rtmv2.RtmGetNextHopInfo
title: RtmGetNextHopInfo function (rtmv2.h)
description: The RtmGetNextHopInfo function returns information about the specified next hop.
helpviewer_keywords: ["RtmGetNextHopInfo","RtmGetNextHopInfo function [RAS]","_rtmv2ref_rtmgetnexthopinfo","rras.rtmgetnexthopinfo","rtmv2/RtmGetNextHopInfo"]
old-location: rras\rtmgetnexthopinfo.htm
tech.root: RRAS
ms.assetid: 45f18cfe-b863-4b78-90e4-c7b25c949834
ms.date: 12/05/2018
ms.keywords: RtmGetNextHopInfo, RtmGetNextHopInfo function [RAS], _rtmv2ref_rtmgetnexthopinfo, rras.rtmgetnexthopinfo, rtmv2/RtmGetNextHopInfo
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
 - RtmGetNextHopInfo
 - rtmv2/RtmGetNextHopInfo
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
 - RtmGetNextHopInfo
---

# RtmGetNextHopInfo function


## -description

The 
<b>RtmGetNextHopInfo</b> function returns information about the specified next hop.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopHandle [in]

Handle to the next hop.

### -param NextHopInfo [out]

On input, <i>NextHopInfo</i> a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure. 




On output, <i>NextHopInfo</i> is filled with the requested next-hop information.

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

When the next hop handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeletenexthop">RtmDeleteNextHop</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthopinfo">RtmReleaseNextHopInfo</a>