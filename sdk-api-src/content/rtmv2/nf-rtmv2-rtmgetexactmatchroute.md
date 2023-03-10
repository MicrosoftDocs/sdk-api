---
UID: NF:rtmv2.RtmGetExactMatchRoute
title: RtmGetExactMatchRoute function (rtmv2.h)
description: The RtmGetExactMatchRoute function searches the routing table for a route that exactly matches the specified route.
helpviewer_keywords: ["RTM_MATCH_FULL","RTM_MATCH_INTERFACE","RTM_MATCH_NEIGHBOUR","RTM_MATCH_NEXTHOP","RTM_MATCH_NONE","RTM_MATCH_OWNER","RTM_MATCH_PREF","RtmGetExactMatchRoute","RtmGetExactMatchRoute function [RAS]","_rtmv2ref_rtmgetexactmatchroute","rras.rtmgetexactmatchroute","rtmv2/RtmGetExactMatchRoute"]
old-location: rras\rtmgetexactmatchroute.htm
tech.root: RRAS
ms.assetid: 5fc9cde7-9912-409f-85ee-c775b4d6ddc0
ms.date: 12/05/2018
ms.keywords: RTM_MATCH_FULL, RTM_MATCH_INTERFACE, RTM_MATCH_NEIGHBOUR, RTM_MATCH_NEXTHOP, RTM_MATCH_NONE, RTM_MATCH_OWNER, RTM_MATCH_PREF, RtmGetExactMatchRoute, RtmGetExactMatchRoute function [RAS], _rtmv2ref_rtmgetexactmatchroute, rras.rtmgetexactmatchroute, rtmv2/RtmGetExactMatchRoute
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
 - RtmGetExactMatchRoute
 - rtmv2/RtmGetExactMatchRoute
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
 - RtmGetExactMatchRoute
---

# RtmGetExactMatchRoute function


## -description

The 
<b>RtmGetExactMatchRoute</b> function searches the routing table for a route that exactly matches the specified route. The route to search for is indicated by a network address, subnet mask, and other route-matching criteria. If an exact match is found, the route information is returned.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestAddress [in]

Pointer to the destination network address.

### -param MatchingFlags [in]

Specifies the criteria to use when searching for the route. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_FULL"></a><a id="rtm_match_full"></a><dl>
<dt><b>RTM_MATCH_FULL</b></dt>
</dl>
</td>
<td width="60%">
Match routes with all criteria.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_INTERFACE"></a><a id="rtm_match_interface"></a><dl>
<dt><b>RTM_MATCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Match routes that are on the same interface.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_NEIGHBOUR"></a><a id="rtm_match_neighbour"></a><dl>
<dt><b>RTM_MATCH_NEIGHBOUR</b></dt>
</dl>
</td>
<td width="60%">
Match routes with the same neighbor.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_NEXTHOP"></a><a id="rtm_match_nexthop"></a><dl>
<dt><b>RTM_MATCH_NEXTHOP</b></dt>
</dl>
</td>
<td width="60%">
Match routes that have the same next hop.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_NONE"></a><a id="rtm_match_none"></a><dl>
<dt><b>RTM_MATCH_NONE</b></dt>
</dl>
</td>
<td width="60%">
Match none of the criteria; all routes for the destination are returned.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_OWNER"></a><a id="rtm_match_owner"></a><dl>
<dt><b>RTM_MATCH_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Match routes with the same owner.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_PREF"></a><a id="rtm_match_pref"></a><dl>
<dt><b>RTM_MATCH_PREF</b></dt>
</dl>
</td>
<td width="60%">
Match routes that have the same preference.

</td>
</tr>
</table>

### -param RouteInfo [in, out]

On input, <i>RouteInfo</i> is a pointer an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure that contains the criteria that specifies the route to find. 




On output, <i>RouteInfo</i> receives the route information for the route that matched the criteria.

### -param InterfaceIndex [in]

If RTM_MATCH_INTERFACE is specified in <i>MatchingFlags</i>, <i>InterfaceIndex</i> specifies the interface on which the route must be present (that is, the route has a next hop on that interface).

### -param TargetViews [in]

Specifies the views from which to return information. If the client specifies RTM_VIEW_MASK_ANY, destination information is returned from all views; however, no view-specific information is returned.

### -param RouteHandle [out]

If a handle must be returned: On input, <i>RouteHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RouteHandle</i> receives a pointer to the route handle; otherwise, <i>RouteHandle</i> remains unchanged.

If a handle does not need to be returned: On input, <i>RouteHandle</i> is <b>NULL</b>.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified route was not found.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

Consider using 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a> if you have no route-matching criteria specified in the <i>MatchingFlags</i> parameter.

The following members of the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure that is passed in the <i>RouteInfo</i> parameter are used to match a route:

<ul>
<li><b>Neighbour</b></li>
<li><b>NextHopsList</b></li>
<li><b>PrefInfo</b></li>
<li><b>RouteOwner</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlessspecificdestination">RtmGetLessSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmisbestroute">RtmIsBestRoute</a>