---
UID: NF:rtmv2.RtmReleaseRoutes
title: RtmReleaseRoutes function (rtmv2.h)
description: The RtmReleaseRoutes function releases the route handles.
helpviewer_keywords: ["RtmReleaseRoutes","RtmReleaseRoutes function [RAS]","_rtmv2ref_rtmreleaseroutes","rras.rtmreleaseroutes","rtmv2/RtmReleaseRoutes"]
old-location: rras\rtmreleaseroutes.htm
tech.root: RRAS
ms.assetid: 4c893144-a2c5-4dc8-83c1-cae0d3024505
ms.date: 12/05/2018
ms.keywords: RtmReleaseRoutes, RtmReleaseRoutes function [RAS], _rtmv2ref_rtmreleaseroutes, rras.rtmreleaseroutes, rtmv2/RtmReleaseRoutes
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
 - RtmReleaseRoutes
 - rtmv2/RtmReleaseRoutes
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
 - RtmReleaseRoutes
---

# RtmReleaseRoutes function


## -description

The 
<b>RtmReleaseRoutes</b> function releases the route handles.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NumRoutes [in]

Specifies the number of routes in <i>RouteHandles</i>.

### -param RouteHandles [in]

Pointer to an array of route handles to release. The handles were obtained with a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>.

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

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreaterouteenum">RtmCreateRouteEnum</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>