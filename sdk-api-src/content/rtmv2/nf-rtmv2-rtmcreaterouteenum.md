---
UID: NF:rtmv2.RtmCreateRouteEnum
title: RtmCreateRouteEnum function (rtmv2.h)
description: The RtmCreateRouteEnum function creates an enumeration of the routes for a particular destination or range of destinations in the routing table. A client can enumerate routes for one or more views, or for all views.
helpviewer_keywords: ["RTM_ENUM_ALL_ROUTES","RTM_ENUM_NEXT","RTM_ENUM_OWN_ROUTES","RTM_ENUM_RANGE","RTM_ENUM_START","RTM_MATCH_FULL","RTM_MATCH_INTERFACE","RTM_MATCH_NEIGHBOUR","RTM_MATCH_NEXTHOP","RTM_MATCH_NONE","RTM_MATCH_OWNER","RTM_MATCH_PREF","RTM_VIEW_MASK_ANY","RTM_VIEW_MASK_MCAST","RTM_VIEW_MASK_UCAST","RtmCreateRouteEnum","RtmCreateRouteEnum function [RAS]","_rtmv2ref_rtmcreaterouteenum","rras.rtmcreaterouteenum","rtmv2/RtmCreateRouteEnum"]
old-location: rras\rtmcreaterouteenum.htm
tech.root: RRAS
ms.assetid: 9d9c35e8-a9d4-4b30-a92c-f3188e11e317
ms.date: 12/05/2018
ms.keywords: RTM_ENUM_ALL_ROUTES, RTM_ENUM_NEXT, RTM_ENUM_OWN_ROUTES, RTM_ENUM_RANGE, RTM_ENUM_START, RTM_MATCH_FULL, RTM_MATCH_INTERFACE, RTM_MATCH_NEIGHBOUR, RTM_MATCH_NEXTHOP, RTM_MATCH_NONE, RTM_MATCH_OWNER, RTM_MATCH_PREF, RTM_VIEW_MASK_ANY, RTM_VIEW_MASK_MCAST, RTM_VIEW_MASK_UCAST, RtmCreateRouteEnum, RtmCreateRouteEnum function [RAS], _rtmv2ref_rtmcreaterouteenum, rras.rtmcreaterouteenum, rtmv2/RtmCreateRouteEnum
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
 - RtmCreateRouteEnum
 - rtmv2/RtmCreateRouteEnum
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
 - RtmCreateRouteEnum
---

# RtmCreateRouteEnum function


## -description

The 
<b>RtmCreateRouteEnum</b> function creates an enumeration of the routes for a particular destination or range of destinations in the routing table. A client can enumerate routes for one or more views, or for all views.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestHandle [in]

Handle to the destination for which to enumerate routes. This parameter is optional, and can be set to <b>NULL</b>; specifying <b>NULL</b> enumerates all routes for all destinations. Specify <b>NULL</b> if <i>EnumFlags</i> contains RTM_ENUM_START.

### -param TargetViews [in]

Specifies the set of views to use when creating the enumeration. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_VIEW_MASK_ANY"></a><a id="rtm_view_mask_any"></a><dl>
<dt><b>RTM_VIEW_MASK_ANY</b></dt>
</dl>
</td>
<td width="60%">
Return destinations from all views. This is the default value.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_VIEW_MASK_UCAST"></a><a id="rtm_view_mask_ucast"></a><dl>
<dt><b>RTM_VIEW_MASK_UCAST</b></dt>
</dl>
</td>
<td width="60%">
Return destinations from the unicast view.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_VIEW_MASK_MCAST"></a><a id="rtm_view_mask_mcast"></a><dl>
<dt><b>RTM_VIEW_MASK_MCAST</b></dt>
</dl>
</td>
<td width="60%">
Return destinations from the multicast view.

</td>
</tr>
</table>

### -param EnumFlags [in]

Specifies which routes to include in the enumeration. Two sets of flags are used; use one flag from each set (such as RTM_ENUM_ALL_ROUTES and RTM_ENUM_START). 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_ALL_ROUTES"></a><a id="rtm_enum_all_routes"></a><dl>
<dt><b>RTM_ENUM_ALL_ROUTES</b></dt>
</dl>
</td>
<td width="60%">
Return all routes.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_OWN_ROUTES"></a><a id="rtm_enum_own_routes"></a><dl>
<dt><b>RTM_ENUM_OWN_ROUTES</b></dt>
</dl>
</td>
<td width="60%">
Return only those routes that the client owns.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_NEXT"></a><a id="rtm_enum_next"></a><dl>
<dt><b>RTM_ENUM_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Enumerate routes starting at the specified address/mask length (such as 10/8). The enumeration continues to the end of the routing table.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_RANGE"></a><a id="rtm_enum_range"></a><dl>
<dt><b>RTM_ENUM_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Enumerate routes in the specified range specified by the address/mask length (such as 10/8).

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_START"></a><a id="rtm_enum_start"></a><dl>
<dt><b>RTM_ENUM_START</b></dt>
</dl>
</td>
<td width="60%">
Enumerate routes starting at 0/0. Specify <b>NULL</b> for <i>NetAddress</i>.

</td>
</tr>
</table>

### -param StartDest [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure that contains the starting address of the enumeration. This parameter is ignored if <i>EnumFlags</i> contains RTM_ENUM_START.

### -param MatchingFlags [in]

Specifies the elements of the route to match. Only routes that match the criteria specified in <i>CriteriaRoute</i> and <i>CriteriaInterface</i> are returned, unless otherwise noted. The following flags are used. 



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
Match routes that are on the same interface. The client can specify <b>NULL</b> for <i>CriteriaRoute</i>.
							

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
Match none of the criteria; all routes for the destination are returned. The <i>CriteriaRoute</i> parameter is ignored if this flag is set.
							

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_MATCH_OWNER"></a><a id="rtm_match_owner"></a><dl>
<dt><b>RTM_MATCH_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Match routes with same owner.

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

### -param CriteriaRoute [in]

Specifies which routes to enumerate. This parameter is optional and can be set to <b>NULL</b> if <i>MatchingFlags</i> contains RTM_MATCH_INTERFACE or RTM_MATCH_NONE.

### -param CriteriaInterface [in]

Pointer to a <b>ULONG</b> that specifies on which interfaces routes should be located. This parameter is ignored unless <i>MatchingFlags</i> contains RTM_MATCH_INTERFACE.

### -param RtmEnumHandle [out]

On input, <i>RtmEnumHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RtmEnumHandle</i> receives a pointer to a handle to the enumeration. Use this handle in all subsequent calls to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>, and 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

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
A parameter contains incorrect information.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified views is not supported.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

If <i>EnumFlags</i> contains RTM_ENUM_RANGE, use <i>NetAddress</i> to specify the range of the routing table to enumerate. For example, if a client sets <i>NetAddress</i> to 10/8, destinations in the range 10.0.0.0/8 to 10.255.255.255/32 are returned.

When the enumeration handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/enumerate-all-routes">Enumerate All Routes</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>