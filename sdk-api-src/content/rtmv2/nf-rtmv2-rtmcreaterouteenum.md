---
UID: NF:rtmv2.RtmCreateRouteEnum
title: RtmCreateRouteEnum function
author: windows-sdk-content
description: The RtmCreateRouteEnum function creates an enumeration of the routes for a particular destination or range of destinations in the routing table. A client can enumerate routes for one or more views, or for all views.
old-location: rras\rtmcreaterouteenum.htm
old-project: RRAS
ms.assetid: 9d9c35e8-a9d4-4b30-a92c-f3188e11e317
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RTM_ENUM_ALL_ROUTES, RTM_ENUM_NEXT, RTM_ENUM_OWN_ROUTES, RTM_ENUM_RANGE, RTM_ENUM_START, RTM_MATCH_FULL, RTM_MATCH_INTERFACE, RTM_MATCH_NEIGHBOUR, RTM_MATCH_NEXTHOP, RTM_MATCH_NONE, RTM_MATCH_OWNER, RTM_MATCH_PREF, RTM_VIEW_MASK_ANY, RTM_VIEW_MASK_MCAST, RTM_VIEW_MASK_UCAST, RtmCreateRouteEnum, RtmCreateRouteEnum function [RAS], _rtmv2ref_rtmcreaterouteenum, rras.rtmcreaterouteenum, rtmv2/RtmCreateRouteEnum
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmCreateRouteEnum
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: ADAM
---

# RtmCreateRouteEnum function


## -description


The 
<b>RtmCreateRouteEnum</b> function creates an enumeration of the routes for a particular destination or range of destinations in the routing table. A client can enumerate routes for one or more views, or for all views.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param OPTIONAL

TBD


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
 


### -param RtmEnumHandle [out]

On input, <i>RtmEnumHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RtmEnumHandle</i> receives a pointer to a handle to the enumeration. Use this handle in all subsequent calls to 
<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>, 
<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>, and 
<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>.


#### - CriteriaInterface [in]

Pointer to a <b>ULONG</b> that specifies on which interfaces routes should be located. This parameter is ignored unless <i>MatchingFlags</i> contains RTM_MATCH_INTERFACE.


#### - CriteriaRoute [in]

Specifies which routes to enumerate. This parameter is optional and can be set to <b>NULL</b> if <i>MatchingFlags</i> contains RTM_MATCH_INTERFACE or RTM_MATCH_NONE.


#### - DestHandle [in]

Handle to the destination for which to enumerate routes. This parameter is optional, and can be set to <b>NULL</b>; specifying <b>NULL</b> enumerates all routes for all destinations. Specify <b>NULL</b> if <i>EnumFlags</i> contains RTM_ENUM_START.


#### - StartDest [in]

Pointer to an 
<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a> structure that contains the starting address of the enumeration. This parameter is ignored if <i>EnumFlags</i> contains RTM_ENUM_START.


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
<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>.

For sample code using this function, see 
<a href="https://msdn.microsoft.com/78a50e4a-f3c7-4a0d-a528-18d35b66369d">Enumerate All Routes</a>.




## -see-also




<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/7d9bf8c0-dc09-440a-b60d-97463c70a745">RTM_ROUTE_INFO</a>



<a href="https://msdn.microsoft.com/87477e25-d4bc-44d2-932b-f266b0bdaafa">RtmDeleteEnumHandle</a>



<a href="https://msdn.microsoft.com/fb3977ef-9edd-4653-b65c-b6d0fb66a785">RtmGetEnumRoutes</a>



<a href="https://msdn.microsoft.com/4c893144-a2c5-4dc8-83c1-cae0d3024505">RtmReleaseRoutes</a>
 

 

