---
UID: NF:rtmv2.RtmInsertInRouteList
title: RtmInsertInRouteList function (rtmv2.h)
description: The RtmInsertInRouteList function inserts the specified set of routes into the client's route list. If a route is already in another list, the route is removed from the old list and inserted into the new one.
helpviewer_keywords: ["RtmInsertInRouteList","RtmInsertInRouteList function [RAS]","_rtmv2ref_rtminsertinroutelist","rras.rtminsertinroutelist","rtmv2/RtmInsertInRouteList"]
old-location: rras\rtminsertinroutelist.htm
tech.root: RRAS
ms.assetid: e0145bdc-5000-429d-8603-1ebc6003a2bc
ms.date: 12/05/2018
ms.keywords: RtmInsertInRouteList, RtmInsertInRouteList function [RAS], _rtmv2ref_rtminsertinroutelist, rras.rtminsertinroutelist, rtmv2/RtmInsertInRouteList
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
 - RtmInsertInRouteList
 - rtmv2/RtmInsertInRouteList
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
 - RtmInsertInRouteList
---

# RtmInsertInRouteList function


## -description

The 
<b>RtmInsertInRouteList</b> function inserts the specified set of routes into the client's route list. If a route is already in another list, the route is removed from the old list and inserted into the new one.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteListHandle [in]

Handle to the route list to which to add routes. Specify <b>NULL</b> to remove the specified routes from their old lists.

### -param NumRoutes [in]

Specifies the number of routes in <i>RouteHandles</i>.

### -param RouteHandles [in]

Pointer to an array of route handles to move from the old list to the new list.

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

## -remarks

When the routes are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/use-a-client-specific-route-list">Use a Client-Specific Route List</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreateroutelist">RtmCreateRouteList</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteroutelist">RtmDeleteRouteList</a>