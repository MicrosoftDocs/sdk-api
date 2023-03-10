---
UID: NF:rtmv2.RtmReleaseRouteInfo
title: RtmReleaseRouteInfo function (rtmv2.h)
description: The RtmReleaseRouteInfo function releases a route structure.
helpviewer_keywords: ["RtmReleaseRouteInfo","RtmReleaseRouteInfo function [RAS]","_rtmv2ref_rtmreleaserouteinfo","rras.rtmreleaserouteinfo","rtmv2/RtmReleaseRouteInfo"]
old-location: rras\rtmreleaserouteinfo.htm
tech.root: RRAS
ms.assetid: 927d2a32-17bc-453c-b65b-144151bea902
ms.date: 12/05/2018
ms.keywords: RtmReleaseRouteInfo, RtmReleaseRouteInfo function [RAS], _rtmv2ref_rtmreleaserouteinfo, rras.rtmreleaserouteinfo, rtmv2/RtmReleaseRouteInfo
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
 - RtmReleaseRouteInfo
 - rtmv2/RtmReleaseRouteInfo
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
 - RtmReleaseRouteInfo
---

# RtmReleaseRouteInfo function


## -description

The 
<b>RtmReleaseRouteInfo</b> function releases a route structure.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteInfo [in]

Pointer to the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure to release. The route was obtained with a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetrouteinfo">RtmGetRouteInfo</a>.

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

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetrouteinfo">RtmGetRouteInfo</a>