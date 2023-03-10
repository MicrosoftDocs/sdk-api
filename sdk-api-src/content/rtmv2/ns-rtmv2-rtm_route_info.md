---
UID: NS:rtmv2._RTM_ROUTE_INFO
title: RTM_ROUTE_INFO (rtmv2.h)
description: The RTM_ROUTE_INFO structure is used to exchange route information with the routing table manager. Do not change the read-only information.
helpviewer_keywords: ["*PRTM_ROUTE_INFO","PRTM_ROUTE_INFO","PRTM_ROUTE_INFO structure pointer [RAS]","RTM_ROUTE_FLAGS_ANY_BCAST","RTM_ROUTE_FLAGS_ANY_MCAST","RTM_ROUTE_FLAGS_ANY_UNICAST","RTM_ROUTE_FLAGS_LIMITED_BC","RTM_ROUTE_FLAGS_LOCAL","RTM_ROUTE_FLAGS_LOCAL_MCAST","RTM_ROUTE_FLAGS_MCAST","RTM_ROUTE_FLAGS_MYSELF","RTM_ROUTE_FLAGS_NET_BCAST","RTM_ROUTE_FLAGS_ONES_NETBC","RTM_ROUTE_FLAGS_ONES_SUBNETBC","RTM_ROUTE_FLAGS_REMOTE","RTM_ROUTE_FLAGS_ZEROS_NETBC","RTM_ROUTE_FLAGS_ZEROS_SUBNETBC","RTM_ROUTE_INFO","RTM_ROUTE_INFO structure [RAS]","RTM_ROUTE_STATE_CREATED","RTM_ROUTE_STATE_DELETED","RTM_ROUTE_STATE_DELETING","_rtmv2ref_rtm_route_info","rras.rtm_route_info","rtmv2/PRTM_ROUTE_INFO","rtmv2/RTM_ROUTE_INFO"]
old-location: rras\rtm_route_info.htm
tech.root: RRAS
ms.assetid: 7d9bf8c0-dc09-440a-b60d-97463c70a745
ms.date: 12/05/2018
ms.keywords: '*PRTM_ROUTE_INFO, PRTM_ROUTE_INFO, PRTM_ROUTE_INFO structure pointer [RAS], RTM_ROUTE_FLAGS_ANY_BCAST, RTM_ROUTE_FLAGS_ANY_MCAST, RTM_ROUTE_FLAGS_ANY_UNICAST, RTM_ROUTE_FLAGS_LIMITED_BC, RTM_ROUTE_FLAGS_LOCAL, RTM_ROUTE_FLAGS_LOCAL_MCAST, RTM_ROUTE_FLAGS_MCAST, RTM_ROUTE_FLAGS_MYSELF, RTM_ROUTE_FLAGS_NET_BCAST, RTM_ROUTE_FLAGS_ONES_NETBC, RTM_ROUTE_FLAGS_ONES_SUBNETBC, RTM_ROUTE_FLAGS_REMOTE, RTM_ROUTE_FLAGS_ZEROS_NETBC, RTM_ROUTE_FLAGS_ZEROS_SUBNETBC, RTM_ROUTE_INFO, RTM_ROUTE_INFO structure [RAS], RTM_ROUTE_STATE_CREATED, RTM_ROUTE_STATE_DELETED, RTM_ROUTE_STATE_DELETING, _rtmv2ref_rtm_route_info, rras.rtm_route_info, rtmv2/PRTM_ROUTE_INFO, rtmv2/RTM_ROUTE_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTM_ROUTE_INFO, *PRTM_ROUTE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_ROUTE_INFO
 - rtmv2/_RTM_ROUTE_INFO
 - PRTM_ROUTE_INFO
 - rtmv2/PRTM_ROUTE_INFO
 - RTM_ROUTE_INFO
 - rtmv2/RTM_ROUTE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ROUTE_INFO
---

# RTM_ROUTE_INFO structure


## -description

The 
<b>RTM_ROUTE_INFO</b> structure is used to exchange route information with the routing table manager. Do not change the read-only information.

## -struct-fields

### -field DestHandle

Handle to the destination that owns the route.

### -field RouteOwner

Handle to the client that owns this route.

### -field Neighbour

Handle to the neighbor that informed the routing table manager of this route. This member is <b>NULL</b> for a link-state protocol.

### -field State

Flags the specify the state of this route. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_STATE_CREATED"></a><a id="rtm_route_state_created"></a><dl>
<dt><b>RTM_ROUTE_STATE_CREATED</b></dt>
</dl>
</td>
<td width="60%">
Route has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_STATE_DELETING"></a><a id="rtm_route_state_deleting"></a><dl>
<dt><b>RTM_ROUTE_STATE_DELETING</b></dt>
</dl>
</td>
<td width="60%">
Route is being deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_STATE_DELETED"></a><a id="rtm_route_state_deleted"></a><dl>
<dt><b>RTM_ROUTE_STATE_DELETED</b></dt>
</dl>
</td>
<td width="60%">
Route has been deleted.

</td>
</tr>
</table>

### -field Flags1

Flags used for compatibility with RTMv1.

### -field Flags

Flags used to specify information about the route. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ANY_BCAST"></a><a id="rtm_route_flags_any_bcast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ANY_BCAST</b></dt>
</dl>
</td>
<td width="60%">
The route is one of the following broadcast types: RTM_ROUTE_FLAGS_LIMITED_BC, RTM_ROUTE_FLAGS_ONES_NETBC, RTM_ROUTE_FLAGS_ONES_SUBNET_BC, RTM_ROUTE_FLAGS_ZEROS_NETBC, RTM_ROUTE_FLAGS_ZEROS_SUBNETBC

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ANY_MCAST"></a><a id="rtm_route_flags_any_mcast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ANY_MCAST</b></dt>
</dl>
</td>
<td width="60%">
The route is one of the following multicast types: RTM_ROUTE_FLAGS_MCAST, RTM_ROUTE_FLAGS_LOCAL_MCAST

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ANY_UNICAST"></a><a id="rtm_route_flags_any_unicast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ANY_UNICAST</b></dt>
</dl>
</td>
<td width="60%">
The route is one of the following unicast types: RTM_ROUTE_FLAGS_LOCAL, RTM_ROUTE_FLAGS_REMOTE, RTM_ROUTE_FLAGS_MYSELF

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_LIMITED_BC"></a><a id="rtm_route_flags_limited_bc"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_LIMITED_BC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this route is a limited broadcast address. Packets to this destination should not be forwarded.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_LOCAL"></a><a id="rtm_route_flags_local"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Indicates a destination is on a directly reachable network.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_LOCAL_MCAST"></a><a id="rtm_route_flags_local_mcast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_LOCAL_MCAST</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this route is a route to a local multicast address.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_MCAST"></a><a id="rtm_route_flags_mcast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_MCAST</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this route is a route to a multicast address.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_MYSELF"></a><a id="rtm_route_flags_myself"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_MYSELF</b></dt>
</dl>
</td>
<td width="60%">
Indicates the destination is one of the router's addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_NET_BCAST"></a><a id="rtm_route_flags_net_bcast"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_NET_BCAST</b></dt>
</dl>
</td>
<td width="60%">
Flag grouping that contains: RTM_ROUTE_FLAGS_ONES_NETBC, RTM_ROUTE_FLAGS_ZEROS_NETBC

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ONES_NETBC"></a><a id="rtm_route_flags_ones_netbc"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ONES_NETBC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the destination matches an interface's <i>all-ones</i> broadcast address. If broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ONES_SUBNETBC"></a><a id="rtm_route_flags_ones_subnetbc"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ONES_SUBNETBC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the destination matches an interface's all-ones subnet broadcast address. If subnet broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_REMOTE"></a><a id="rtm_route_flags_remote"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_REMOTE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the destination is not on a directly reachable network.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ZEROS_SUBNETBC"></a><a id="rtm_route_flags_zeros_subnetbc"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ZEROS_SUBNETBC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the destination matches an interface's <i>all-zeros</i> subnet broadcast address. If subnet broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_FLAGS_ZEROS_NETBC"></a><a id="rtm_route_flags_zeros_netbc"></a><dl>
<dt><b>RTM_ROUTE_FLAGS_ZEROS_NETBC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the destination matches an interface's all-zeros broadcast address. If broadcast forwarding is enabled, packets should be received and resent out all appropriate interfaces.

</td>
</tr>
</table>

### -field PrefInfo

Specifies the preference and metric information for this route.

### -field BelongsToViews

Specifies the views in which this route is included.

### -field EntitySpecificInfo

Contains the client-specific information for the client that owns this route.

### -field NextHopsList

Specifies a list of equal-cost next hops.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_list">RTM_NEXTHOP_LIST</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_pref_info">RTM_PREF_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmaddroutetodest">RtmAddRouteToDest</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreaterouteenum">RtmCreateRouteEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchroute">RtmGetExactMatchRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetrouteinfo">RtmGetRouteInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetroutepointer">RtmGetRoutePointer</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockroute">RtmLockRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaserouteinfo">RtmReleaseRouteInfo</a>