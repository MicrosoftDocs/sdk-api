---
UID: NF:rtmv2.RtmGetEnumDests
title: RtmGetEnumDests function (rtmv2.h)
description: The RtmGetEnumDests function retrieves the next set of destinations in the specified enumeration.
helpviewer_keywords: ["RtmGetEnumDests","RtmGetEnumDests function [RAS]","_rtmv2ref_rtmgetenumdests","rras.rtmgetenumdests","rtmv2/RtmGetEnumDests"]
old-location: rras\rtmgetenumdests.htm
tech.root: RRAS
ms.assetid: f793b54e-9591-4b9f-b109-8487013c7af5
ms.date: 12/05/2018
ms.keywords: RtmGetEnumDests, RtmGetEnumDests function [RAS], _rtmv2ref_rtmgetenumdests, rras.rtmgetenumdests, rtmv2/RtmGetEnumDests
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
 - RtmGetEnumDests
 - rtmv2/RtmGetEnumDests
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
 - RtmGetEnumDests
---

# RtmGetEnumDests function


## -description

The 
<b>RtmGetEnumDests</b> function retrieves the next set of destinations in the specified enumeration.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumHandle [in]

Handle to the destination enumeration.

### -param NumDests [in, out]

On input, <i>NumDests</i> is a pointer to a <b>UINT</b> value specifying the maximum number of destinations that can be received by <i>DestInfos</i>. On output, <i>NumDests</i> receives the actual number of destinations received by <i>DestInfos</i>.

### -param DestInfos [out]

On input, <i>DestInfos</i> is a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a> structure. 




On output, <i>DestInfos</i> receives an array of handles to destinations.

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
The value pointed to by <i>NumRoutes</i> is larger than the maximum number of routes a client is allowed to retrieve with one call. Check 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_regn_profile">RTM_REGN_PROFILE</a> for the maximum number of destinations that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more destinations to enumerate.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The structure pointed to by <i>DestInfos</i>  is a variable-sized structure. If the client specifies more than one view with <i>TargetViews</i>, the size of <i>DestInfos</i> increases for each view. Use the 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_size_of_dest_info">RTM_SIZE_OF_DEST_INFO</a> macro to determine how large a <i>DestInfos</i> structure to allocate before calling this function. Use the value specified for <i>TargetViews</i> as a parameter to 
<b>RTM_SIZE_OF_DEST_INFO</b>.

When the destinations are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/enumerate-all-destinations">Enumerate All Destinations</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_dest_info">RTM_DEST_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatedestenum">RtmCreateDestEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>