---
UID: NF:rtmv2.RtmGetMostSpecificDestination
title: RtmGetMostSpecificDestination function (rtmv2.h)
description: The RtmGetMostSpecificDestination function searches the routing table for a destination with the exact match for a specified network address and subnet mask; if the exact match is not found, the best prefix is matched.
helpviewer_keywords: ["RtmGetMostSpecificDestination","RtmGetMostSpecificDestination function [RAS]","_rtmv2ref_rtmgetmostspecificdestination","rras.rtmgetmostspecificdestination","rtmv2/RtmGetMostSpecificDestination"]
old-location: rras\rtmgetmostspecificdestination.htm
tech.root: RRAS
ms.assetid: 682a41bb-c623-4c01-856a-5f1923c6cab8
ms.date: 12/05/2018
ms.keywords: RtmGetMostSpecificDestination, RtmGetMostSpecificDestination function [RAS], _rtmv2ref_rtmgetmostspecificdestination, rras.rtmgetmostspecificdestination, rtmv2/RtmGetMostSpecificDestination
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
 - RtmGetMostSpecificDestination
 - rtmv2/RtmGetMostSpecificDestination
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
 - RtmGetMostSpecificDestination
---

# RtmGetMostSpecificDestination function


## -description

The 
<b>RtmGetMostSpecificDestination</b> function searches the routing table for a destination with the exact match for a specified network address and subnet mask; if the exact match is not found, the best prefix is matched. The destination information is returned.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestAddress [in]

Pointer to the destination network address.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified destination was not found.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The <i>DestInfo</i> structure is a variable-sized structure. If the client specifies more than one view with <i>TargetViews</i>, the size of <i>DestInfo</i> increases for each view. Use the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_size_of_dest_info">RTM_SIZE_OF_DEST_INFO</a> macro to determine how much memory to allocate for the <i>DestInfo</i> structure before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination">Search for Routes Using a Prefix Tree</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchdestination">RtmGetExactMatchDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetexactmatchroute">RtmGetExactMatchRoute</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlessspecificdestination">RtmGetLessSpecificDestination</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmisbestroute">RtmIsBestRoute</a>