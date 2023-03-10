---
UID: NF:rtmv2.RtmGetRouteInfo
title: RtmGetRouteInfo function (rtmv2.h)
description: The RtmGetRouteInfo function returns information for the specified route.
helpviewer_keywords: ["RtmGetRouteInfo","RtmGetRouteInfo function [RAS]","_rtmv2ref_rtmgetrouteinfo","rras.rtmgetrouteinfo","rtmv2/RtmGetRouteInfo"]
old-location: rras\rtmgetrouteinfo.htm
tech.root: RRAS
ms.assetid: 13fc70de-f6cd-4e7a-b79d-c2fe811e08a4
ms.date: 12/05/2018
ms.keywords: RtmGetRouteInfo, RtmGetRouteInfo function [RAS], _rtmv2ref_rtmgetrouteinfo, rras.rtmgetrouteinfo, rtmv2/RtmGetRouteInfo
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
 - RtmGetRouteInfo
 - rtmv2/RtmGetRouteInfo
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
 - RtmGetRouteInfo
---

# RtmGetRouteInfo function


## -description

The 
<b>RtmGetRouteInfo</b> function returns information for the specified route.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteHandle [in]

Handle to the route to find.

### -param RouteInfo [out]

If a pointer must be returned: On input, <i>RouteInfo</i> is a pointer to <b>NULL</b>. On output, <i>RouteInfo</i> receives a pointer to the route; otherwise, <i>RouteInfo</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>RouteInfo</i> is <b>NULL</b>.

### -param DestAddress [out]

If a pointer must be returned: On input, <i>DestAddress</i> is a pointer to <b>NULL</b>. On output, <i>DestAddress</i> receives a pointer to the destination's 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure; otherwise, <i>DestAddress</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>DestAddress</i> is <b>NULL</b>.

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

When the routes are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaserouteinfo">RtmReleaseRouteInfo</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaserouteinfo">RtmReleaseRouteInfo</a>