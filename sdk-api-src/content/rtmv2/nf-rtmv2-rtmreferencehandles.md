---
UID: NF:rtmv2.RtmReferenceHandles
title: RtmReferenceHandles function (rtmv2.h)
description: The RtmReferenceHandles function increases the reference count for objects pointed to by one or more handles that the routing manager used to access those objects.
helpviewer_keywords: ["RtmReferenceHandles","RtmReferenceHandles function [RAS]","_rtmv2ref_rtmreferencehandles","rras.rtmreferencehandles","rtmv2/RtmReferenceHandles"]
old-location: rras\rtmreferencehandles.htm
tech.root: RRAS
ms.assetid: 99031574-a941-451f-ad2e-b99044c9c716
ms.date: 12/05/2018
ms.keywords: RtmReferenceHandles, RtmReferenceHandles function [RAS], _rtmv2ref_rtmreferencehandles, rras.rtmreferencehandles, rtmv2/RtmReferenceHandles
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
 - RtmReferenceHandles
 - rtmv2/RtmReferenceHandles
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
 - RtmReferenceHandles
---

# RtmReferenceHandles function


## -description

The 
<b>RtmReferenceHandles</b> function increases the reference count for objects pointed to by one or more handles that the routing manager used to access those objects. A client should use this function when the client must keep a handle but release the rest of the information structure associated with the handle.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NumHandles [in]

Specifies the number of handles in <i>RtmHandles</i>.

### -param RtmHandles [in]

Array of handles to increase the reference count for.

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
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

A client must always call this function when caching a handle returned by the routing table manager. This notifies the routing table manager that it should not destroy the object the handle refers to until the handle is released by the client.

When a client must release the handle, the client must call the appropriate release function, based on the type of handle. For example, to release a route, call 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasechangeddests">RtmReleaseChangedDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedestinfo">RtmReleaseDestInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentityinfo">RtmReleaseEntityInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthopinfo">RtmReleaseNextHopInfo</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaserouteinfo">RtmReleaseRouteInfo</a>