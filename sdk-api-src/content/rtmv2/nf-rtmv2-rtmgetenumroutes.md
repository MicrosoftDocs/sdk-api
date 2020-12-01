---
UID: NF:rtmv2.RtmGetEnumRoutes
title: RtmGetEnumRoutes function (rtmv2.h)
description: The RtmGetEnumRoutes function retrieves the next set of routes in the specified enumeration.
helpviewer_keywords: ["RtmGetEnumRoutes","RtmGetEnumRoutes function [RAS]","_rtmv2ref_rtmgetenumroutes","rras.rtmgetenumroutes","rtmv2/RtmGetEnumRoutes"]
old-location: rras\rtmgetenumroutes.htm
tech.root: RRAS
ms.assetid: fb3977ef-9edd-4653-b65c-b6d0fb66a785
ms.date: 12/05/2018
ms.keywords: RtmGetEnumRoutes, RtmGetEnumRoutes function [RAS], _rtmv2ref_rtmgetenumroutes, rras.rtmgetenumroutes, rtmv2/RtmGetEnumRoutes
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
 - RtmGetEnumRoutes
 - rtmv2/RtmGetEnumRoutes
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
 - RtmGetEnumRoutes
---

# RtmGetEnumRoutes function


## -description

The 
<b>RtmGetEnumRoutes</b> function retrieves the next set of routes in the specified enumeration.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumHandle [in]

Handle to the route enumeration.

### -param NumRoutes [in, out]

On input, <i>NumRoutes</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of routes that can be received by <i>RouteHandles</i>. 




On output, <i>NumRoutes</i> receives the actual number of routes received by <i>RouteHandles</i>.

### -param RouteHandles [out]

On input, <i>RouteHandles</i> is a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure. 




On output, <i>RouteHandles</i> receives an array of handles to routes.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>NumRoutes</i> is larger than the maximum number of routes a client is allowed to retrieve with one call. Check 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_regn_profile">RTM_REGN_PROFILE</a> for the maximum number of routes that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more routes to enumerate.

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

When the routes are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/enumerate-all-routes">Enumerate All Routes</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreaterouteenum">RtmCreateRouteEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>