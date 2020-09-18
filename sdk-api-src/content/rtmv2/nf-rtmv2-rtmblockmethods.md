---
UID: NF:rtmv2.RtmBlockMethods
title: RtmBlockMethods function (rtmv2.h)
description: The RtmBlockMethods function blocks or unblocks the execution of methods for a specified destination, route, or next hop, or for all destinations, routes, and next hops.
helpviewer_keywords: ["DEST_TYPE","NEXTHOP_TYPE","ROUTE_TYPE","RTM_BLOCK_METHODS","RTM_RESUME_METHODS","RtmBlockMethods","RtmBlockMethods function [RAS]","_rtmv2ref_rtmblockmethods","rras.rtmblockmethods","rtmv2/RtmBlockMethods"]
old-location: rras\rtmblockmethods.htm
tech.root: RRAS
ms.assetid: 492bb2bf-5b35-4eef-a039-3d3e1137220f
ms.date: 12/05/2018
ms.keywords: DEST_TYPE, NEXTHOP_TYPE, ROUTE_TYPE, RTM_BLOCK_METHODS, RTM_RESUME_METHODS, RtmBlockMethods, RtmBlockMethods function [RAS], _rtmv2ref_rtmblockmethods, rras.rtmblockmethods, rtmv2/RtmBlockMethods
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
 - RtmBlockMethods
 - rtmv2/RtmBlockMethods
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
 - RtmBlockMethods
---

# RtmBlockMethods function


## -description

The 
<b>RtmBlockMethods</b> function blocks or unblocks the execution of methods for a specified destination, route, or next hop, or for all destinations, routes, and next hops.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param TargetHandle [in]

Handle to a destination, route, or next hop for which to block methods. This parameter is optional and can be set to <b>NULL</b> to block methods for all targets.

### -param TargetType [in]

Specifies the type of the handle in <i>TargetHandle</i>. This parameter is optional and can be set to <b>NULL</b> to block methods for all targets. The following flags are used. 



<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEST_TYPE"></a><a id="dest_type"></a><dl>
<dt><b>DEST_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>TargetHandle</i> is a destination.

</td>
</tr>
<tr>
<td width="40%"><a id="NEXTHOP_TYPE"></a><a id="nexthop_type"></a><dl>
<dt><b>NEXTHOP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>TargetHandle</i> is a next hop.

</td>
</tr>
<tr>
<td width="40%"><a id="ROUTE_TYPE"></a><a id="route_type"></a><dl>
<dt><b>ROUTE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>TargetHandle</i> is a route.

</td>
</tr>
</table>

### -param BlockingFlag [in]

Specifies whether to block or unblock methods. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_BLOCK_METHODS"></a><a id="rtm_block_methods"></a><dl>
<dt><b>RTM_BLOCK_METHODS</b></dt>
</dl>
</td>
<td width="60%">
Block methods for the specified target.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_RESUME_METHODS"></a><a id="rtm_resume_methods"></a><dl>
<dt><b>RTM_RESUME_METHODS</b></dt>
</dl>
</td>
<td width="60%">
Unblock methods for the specified target.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is the following error code.

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

## -remarks

Currently, this function does not support blocking methods for a specific destination, route, or next hop.

Methods are typically blocked when client-specific data in the route is being changed; a client blocks methods, rearranges data, and then unblocks methods.

Clients should only block methods for a short period of time. If a second client calls 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtminvokemethod">RtmInvokeMethod</a> and the first client's methods are blocked, 
<b>RtmInvokeMethod</b> does not return until methods are unblocked and the function call is completed.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetentitymethods">RtmGetEntityMethods</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtminvokemethod">RtmInvokeMethod</a>