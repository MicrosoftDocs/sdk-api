---
UID: NF:rtmv2.RtmDeleteEnumHandle
title: RtmDeleteEnumHandle function (rtmv2.h)
description: The RtmDeleteEnumHandle function deletes the specified enumeration handle and frees all resources allocated for the enumeration.
helpviewer_keywords: ["RtmDeleteEnumHandle","RtmDeleteEnumHandle function [RAS]","_rtmv2ref_rtmdeleteenumhandle","rras.rtmdeleteenumhandle","rtmv2/RtmDeleteEnumHandle"]
old-location: rras\rtmdeleteenumhandle.htm
tech.root: RRAS
ms.assetid: 87477e25-d4bc-44d2-932b-f266b0bdaafa
ms.date: 12/05/2018
ms.keywords: RtmDeleteEnumHandle, RtmDeleteEnumHandle function [RAS], _rtmv2ref_rtmdeleteenumhandle, rras.rtmdeleteenumhandle, rtmv2/RtmDeleteEnumHandle
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
 - RtmDeleteEnumHandle
 - rtmv2/RtmDeleteEnumHandle
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
 - RtmDeleteEnumHandle
---

# RtmDeleteEnumHandle function


## -description

The 
<b>RtmDeleteEnumHandle</b> function deletes the specified enumeration handle and frees all resources allocated for the enumeration.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumHandle [in]

Handle to be released. Any resources associated with the handle are also freed.

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

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatedestenum">RtmCreateDestEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreatenexthopenum">RtmCreateNextHopEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreaterouteenum">RtmCreateRouteEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreateroutelistenum">RtmCreateRouteListEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumnexthops">RtmGetEnumNextHops</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasedests">RtmReleaseDests</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseroutes">RtmReleaseRoutes</a>