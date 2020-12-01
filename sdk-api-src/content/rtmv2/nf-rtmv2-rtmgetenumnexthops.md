---
UID: NF:rtmv2.RtmGetEnumNextHops
title: RtmGetEnumNextHops function (rtmv2.h)
description: The RtmGetEnumNextHops function retrieves the next set of next hops in the specified enumeration.
helpviewer_keywords: ["RtmGetEnumNextHops","RtmGetEnumNextHops function [RAS]","_rtmv2ref_rtmgetenumnexthops","rras.rtmgetenumnexthops","rtmv2/RtmGetEnumNextHops"]
old-location: rras\rtmgetenumnexthops.htm
tech.root: RRAS
ms.assetid: 3e1a6064-6ba0-4ed8-b6df-1c347b098807
ms.date: 12/05/2018
ms.keywords: RtmGetEnumNextHops, RtmGetEnumNextHops function [RAS], _rtmv2ref_rtmgetenumnexthops, rras.rtmgetenumnexthops, rtmv2/RtmGetEnumNextHops
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
 - RtmGetEnumNextHops
 - rtmv2/RtmGetEnumNextHops
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
 - RtmGetEnumNextHops
---

# RtmGetEnumNextHops function


## -description

The 
<b>RtmGetEnumNextHops</b> function retrieves the next set of next hops in the specified enumeration.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumHandle [in]

Handle to the next-hop enumeration.

### -param NumNextHops [in, out]

On input, <i>NumNextHops</i> is a pointer to a <b>UINT</b> value specifying the maximum number of next hops that can be received by <i>NextHopHandles</i>. 




On output, <i>NumNextHops</i> receives the actual number of next hops received by <i>NextHopHandles</i>.

### -param NextHopHandles [out]

On input, <i>NextHopHandles</i> pointers to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_nexthop_info">RTM_NEXTHOP_INFO</a> structure. 




On output, <i>NextHopHandles</i> receives an array of handles to next hops.

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
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_regn_profile">RTM_REGN_PROFILE</a> for the maximum number of next hops that the client is allowed to retrieve with one call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more next hops to enumerate.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

When the next hops are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatenexthopenum">RtmCreateNextHopEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>