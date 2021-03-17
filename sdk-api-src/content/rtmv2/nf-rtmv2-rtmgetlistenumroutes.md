---
UID: NF:rtmv2.RtmGetListEnumRoutes
title: RtmGetListEnumRoutes function (rtmv2.h)
description: The RtmGetListEnumRoutes function enumerates a set of routes in a specified route list.
helpviewer_keywords: ["RtmGetListEnumRoutes","RtmGetListEnumRoutes function [RAS]","_rtmv2ref_rtmgetlistenumroutes","rras.rtmgetlistenumroutes","rtmv2/RtmGetListEnumRoutes"]
old-location: rras\rtmgetlistenumroutes.htm
tech.root: RRAS
ms.assetid: 9ee40466-63e9-40c4-82bf-45f819d0ae58
ms.date: 12/05/2018
ms.keywords: RtmGetListEnumRoutes, RtmGetListEnumRoutes function [RAS], _rtmv2ref_rtmgetlistenumroutes, rras.rtmgetlistenumroutes, rtmv2/RtmGetListEnumRoutes
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
 - RtmGetListEnumRoutes
 - rtmv2/RtmGetListEnumRoutes
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
 - RtmGetListEnumRoutes
---

# RtmGetListEnumRoutes function


## -description

The 
<b>RtmGetListEnumRoutes</b> function enumerates a set of routes in a specified route list.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumHandle [in]

Handle to the route list to enumerate.

### -param NumRoutes [in, out]

On input, <i>NumRoutes</i> is a pointer to a <b>UINT</b> value that specifies the maximum number of routes that can be received by <i>RouteHandles</i>. 




On output, <i>NumRoutes</i> receives the actual number of routes received by <i>RouteHandles</i>.

### -param RouteHandles [out]

On input, <i>DestInfo</i> is a pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structures. 




On output, <i>DestInfo</i> is filled with the requested destination information.

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
</table>
 


<div> </div>

## -remarks

Call this function repeatedly to retrieve all routes.

There are no more routes to enumerate when the routing table manager returns zero in <i>NumRoutes</i>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/use-a-client-specific-route-list">Use a Client-Specific Route List</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreateroutelistenum">RtmCreateRouteListEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>