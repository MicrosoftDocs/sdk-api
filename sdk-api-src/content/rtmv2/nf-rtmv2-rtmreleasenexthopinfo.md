---
UID: NF:rtmv2.RtmReleaseNextHopInfo
title: RtmReleaseNextHopInfo function (rtmv2.h)
description: The RtmReleaseNextHopInfo function releases a next-hop structure.
helpviewer_keywords: ["RtmReleaseNextHopInfo","RtmReleaseNextHopInfo function [RAS]","_rtmv2ref_rtmreleasenexthopinfo","rras.rtmreleasenexthopinfo","rtmv2/RtmReleaseNextHopInfo"]
old-location: rras\rtmreleasenexthopinfo.htm
tech.root: RRAS
ms.assetid: 1c5a9b72-8605-4c54-bc44-b7a1a4e1b367
ms.date: 12/05/2018
ms.keywords: RtmReleaseNextHopInfo, RtmReleaseNextHopInfo function [RAS], _rtmv2ref_rtmreleasenexthopinfo, rras.rtmreleasenexthopinfo, rtmv2/RtmReleaseNextHopInfo
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
 - RtmReleaseNextHopInfo
 - rtmv2/RtmReleaseNextHopInfo
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
 - RtmReleaseNextHopInfo
---

# RtmReleaseNextHopInfo function


## -description

The 
<b>RtmReleaseNextHopInfo</b> function releases a next-hop structure.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NextHopInfo [in]

Pointer to the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure to release. The next hop was obtained with a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthopinfo">RtmGetNextHopInfo</a>.

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

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmfindnexthop">RtmFindNextHop</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetnexthopinfo">RtmGetNextHopInfo</a>