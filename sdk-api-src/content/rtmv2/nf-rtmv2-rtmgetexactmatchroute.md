---
UID: NF:rtmv2.RtmGetExactMatchRoute
title: RtmGetExactMatchRoute function
author: windows-driver-content
description: The RtmGetExactMatchRoute function searches the routing table for a route that exactly matches the specified route.
old-location: rras\rtmgetexactmatchroute.htm
old-project: RRAS
ms.assetid: 5fc9cde7-9912-409f-85ee-c775b4d6ddc0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RTM_MATCH_FULL, RTM_MATCH_INTERFACE, RTM_MATCH_NEIGHBOUR, RTM_MATCH_NEXTHOP, RTM_MATCH_NONE, RTM_MATCH_OWNER, RTM_MATCH_PREF, RtmGetExactMatchRoute, RtmGetExactMatchRoute function [RAS], _rtmv2ref_rtmgetexactmatchroute, rras.rtmgetexactmatchroute, rtmv2/RtmGetExactMatchRoute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmGetExactMatchRoute
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# RtmGetExactMatchRoute function


## -description


The 
<b>RtmGetExactMatchRoute</b> function searches the routing table for a route that exactly matches the specified route. The route to search for is indicated by a network address, subnet mask, and other route-matching criteria. If an exact match is found, the route information is returned.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


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
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure that contains the criteria that specifies the route to find. 




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
<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a> if you have no route-matching criteria specified in the <i>MatchingFlags</i> parameter.

The following members of the 
<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a> structure that is passed in the <i>RouteInfo</i> parameter are used to match a route:

<ul>
<li><b>Neighbour</b></li>
<li><b>NextHopsList</b></li>
<li><b>PrefInfo</b></li>
<li><b>RouteOwner</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/0cbb24f4-30f4-41be-aea2-36474760d374">RtmGetExactMatchDestination</a>



<a href="https://msdn.microsoft.com/b6ff1b1f-fd0e-4cfb-9030-67e27e8578f6">RtmGetLessSpecificDestination</a>



<a href="https://msdn.microsoft.com/682a41bb-c623-4c01-856a-5f1923c6cab8">RtmGetMostSpecificDestination</a>



<a href="https://msdn.microsoft.com/4c4b72a8-7a6c-4216-af2d-8dee55b910af">RtmIsBestRoute</a>
 

 

