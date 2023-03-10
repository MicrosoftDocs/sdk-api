---
UID: NF:rtmv2.RtmCreateDestEnum
title: RtmCreateDestEnum function (rtmv2.h)
description: The RtmCreateDestEnum function starts an enumeration of the destinations in the routing table. A client can enumerate destinations for one or more views, or for all views.
helpviewer_keywords: ["RTM_ENUM_ALL_DESTS","RTM_ENUM_NEXT","RTM_ENUM_OWN_DESTS","RTM_ENUM_RANGE","RTM_ENUM_START","RTM_VIEW_MASK_ANY","RTM_VIEW_MASK_MCAST","RTM_VIEW_MASK_UCAST","RtmCreateDestEnum","RtmCreateDestEnum function [RAS]","_rtmv2ref_rtmcreatedestenum","rras.rtmcreatedestenum","rtmv2/RtmCreateDestEnum"]
old-location: rras\rtmcreatedestenum.htm
tech.root: RRAS
ms.assetid: 6efea7b4-dd44-4b08-999d-62e7f660ed64
ms.date: 12/05/2018
ms.keywords: RTM_ENUM_ALL_DESTS, RTM_ENUM_NEXT, RTM_ENUM_OWN_DESTS, RTM_ENUM_RANGE, RTM_ENUM_START, RTM_VIEW_MASK_ANY, RTM_VIEW_MASK_MCAST, RTM_VIEW_MASK_UCAST, RtmCreateDestEnum, RtmCreateDestEnum function [RAS], _rtmv2ref_rtmcreatedestenum, rras.rtmcreatedestenum, rtmv2/RtmCreateDestEnum
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
 - RtmCreateDestEnum
 - rtmv2/RtmCreateDestEnum
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
 - RtmCreateDestEnum
---

# RtmCreateDestEnum function


## -description

The 
<b>RtmCreateDestEnum</b> function starts an enumeration of the destinations in the routing table. A client can enumerate destinations for one or more views, or for all views.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

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

Specifies which destinations to include in the enumeration. Two sets of flags are used; use one flag from each set (for example, use RTM_ENUM_ALL_DESTS and RTM_ENUM_START). 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_ALL_DESTS"></a><a id="rtm_enum_all_dests"></a><dl>
<dt><b>RTM_ENUM_ALL_DESTS</b></dt>
</dl>
</td>
<td width="60%">
Return all destinations.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_OWN_DESTS"></a><a id="rtm_enum_own_dests"></a><dl>
<dt><b>RTM_ENUM_OWN_DESTS</b></dt>
</dl>
</td>
<td width="60%">
Return destinations for which the client owns the best route to a destination in any of the specified views.

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
Enumerate destinations starting at the specified address/mask length (such as 10/8). The enumeration continues to the end of the routing table.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_RANGE"></a><a id="rtm_enum_range"></a><dl>
<dt><b>RTM_ENUM_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Enumerate destinations in the range specified by the address/mask length (such as 10/8).

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_START"></a><a id="rtm_enum_start"></a><dl>
<dt><b>RTM_ENUM_START</b></dt>
</dl>
</td>
<td width="60%">
Enumerate destinations starting at 0/0. Specify <b>NULL</b> for <i>NetAddress</i>.

</td>
</tr>
</table>

### -param NetAddress [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure that contains the starting address of the enumeration. Specify <b>NULL</b> if <i>EnumFlags</i> contains RTM_ENUM_START.

### -param ProtocolId [in]

Specifies the protocol identifier used to determine the best route information returned by the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a> function. The <i>ProtocolID</i> is not part of the search criteria. The routing table manager uses this identifier to determine which route information to return (for example, if a client specifies the RIP protocol identifier, the best RIP route is returned, even if a non-RIP route is the best route to the destination). 




Specify RTM_BEST_PROTOCOL to return a route regardless of which protocol owns it. Specify RTM_THIS_PROTOCOL to return the best route for the calling protocol.

### -param RtmEnumHandle [out]

On input, <i>RtmEnumHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RtmEnumHandle</i> receives a pointer to a handle to the enumeration. Use this handle in all subsequent calls to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>, and 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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

## -remarks

If <i>EnumFlags</i> contains RTM_ENUM_RANGE, use <i>NetAddress</i> to specify the range of the routing table to enumerate. For example, if a client sets <i>NetAddress</i> to 10/8, destinations in the range 10.0.0.0/8 to 10.255.255.255/32 are returned.

When the enumeration handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/enumerate-all-destinations">Enumerate All Destinations</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>