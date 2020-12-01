---
UID: NF:rtmv2.RtmIsBestRoute
title: RtmIsBestRoute function (rtmv2.h)
description: The RtmIsBestRoute function returns the set of views in which the specified route is the best route to a destination.
helpviewer_keywords: ["RtmIsBestRoute","RtmIsBestRoute function [RAS]","_rtmv2ref_rtmisbestroute","rras.rtmisbestroute","rtmv2/RtmIsBestRoute"]
old-location: rras\rtmisbestroute.htm
tech.root: RRAS
ms.assetid: 4c4b72a8-7a6c-4216-af2d-8dee55b910af
ms.date: 12/05/2018
ms.keywords: RtmIsBestRoute, RtmIsBestRoute function [RAS], _rtmv2ref_rtmisbestroute, rras.rtmisbestroute, rtmv2/RtmIsBestRoute
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
 - RtmIsBestRoute
 - rtmv2/RtmIsBestRoute
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
 - RtmIsBestRoute
---

# RtmIsBestRoute function


## -description

The 
<b>RtmIsBestRoute</b> function returns the set of views in which the specified route is the best route to a destination.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteHandle [in]

Handle to the route to check.

### -param BestInViews [out]

Receives a pointer to the set of views for which the specified route is the best route.

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

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchroute">RtmGetExactMatchRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlessspecificdestination">RtmGetLessSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a>