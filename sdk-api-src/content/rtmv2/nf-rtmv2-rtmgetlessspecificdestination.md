---
UID: NF:rtmv2.RtmGetLessSpecificDestination
title: RtmGetLessSpecificDestination function (rtmv2.h)
description: The RtmGetLessSpecificDestination function searches the routing table for a destination with the next-best-match (longest) prefix, given a destination prefix. The requested destination information is returned.
helpviewer_keywords: ["RtmGetLessSpecificDestination","RtmGetLessSpecificDestination function [RAS]","_rtmv2ref_rtmgetlessspecificdestination","rras.rtmgetlessspecificdestination","rtmv2/RtmGetLessSpecificDestination"]
old-location: rras\rtmgetlessspecificdestination.htm
tech.root: RRAS
ms.assetid: b6ff1b1f-fd0e-4cfb-9030-67e27e8578f6
ms.date: 12/05/2018
ms.keywords: RtmGetLessSpecificDestination, RtmGetLessSpecificDestination function [RAS], _rtmv2ref_rtmgetlessspecificdestination, rras.rtmgetlessspecificdestination, rtmv2/RtmGetLessSpecificDestination
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
 - RtmGetLessSpecificDestination
 - rtmv2/RtmGetLessSpecificDestination
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
 - RtmGetLessSpecificDestination
---

# RtmGetLessSpecificDestination function


## -description

The 
<b>RtmGetLessSpecificDestination</b> function searches the routing table for a destination with the next-best-match (longest) prefix, given a destination prefix. The requested destination information is returned.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestHandle [in]

Handle to the destination.

### -param ProtocolId [in]

Specifies the protocol identifier. The <i>ProtocolID</i> is not part of the search criteria. The routing table manager uses this identifier to determine which route information to return. For example, if a client specifies the RIP protocol identifier, the best RIP route is returned, even if a non-RIP route is the best route to the destination. 




Specify RTM_BEST_PROTOCOL to return a route regardless of which protocol owns it. Specify RTM_THIS_PROTOCOL to return the best route for the calling protocol.

### -param TargetViews [in]

Specifies the views from which to return information. If the client specifies RTM_VIEW_MASK_ANY, destination information is returned from all views; however, no view-specific information is returned.

### -param DestInfo [out]

On input, <i>DestInfo</i> is a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure. 




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
A parameter contains incorrect information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The next best destination cannot be found.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The <i>DestInfo</i> parameter is a variable-sized 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure. If the client specifies more than one view using <i>TargetViews</i>, the size of <i>DestInfo</i> increases for each view. Use the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_size_of_dest_info">RTM_SIZE_OF_DEST_INFO</a> macro to determine how much memory to allocate for the <i>DestInfo</i> structure before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

The 
<b>RtmGetLessSpecificDestination</b> function is used after a call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a> to return the next-best match for a destination. This call is also used after a prior call to 
<b>RtmGetLessSpecificDestination</b> to return the next successive less-specific match. Clients can use this function to "walk up" the prefix tree for a destination.

This call is also used after calls to functions that return an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure, such as 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetdestinfo">RtmGetDestInfo</a> and 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>.

The 
<b>RtmGetLessSpecificDestination</b> function returns matches until it reaches the default route, if it exists. Once the default route is found, 
<b>RtmGetLessSpecificDestination</b> returns ERROR_NOT_FOUND.

One common use for the 
<b>RtmGetLessSpecificDestination</b> and 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a> functions, is to retrieve each of the matching destinations.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination">Search for Routes Using a Prefix Tree</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchroute">RtmGetExactMatchRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetmostspecificdestination">RtmGetMostSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmisbestroute">RtmIsBestRoute</a>