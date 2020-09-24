---
UID: NF:rtmv2.RtmReleaseEntityInfo
title: RtmReleaseEntityInfo function (rtmv2.h)
description: The RtmReleaseEntityInfo function releases a client structure.
helpviewer_keywords: ["RtmReleaseEntityInfo","RtmReleaseEntityInfo function [RAS]","_rtmv2ref_rtmreleaseentityinfo","rras.rtmreleaseentityinfo","rtmv2/RtmReleaseEntityInfo"]
old-location: rras\rtmreleaseentityinfo.htm
tech.root: RRAS
ms.assetid: ea72dde4-2d04-4ceb-b718-3ee96bf70464
ms.date: 12/05/2018
ms.keywords: RtmReleaseEntityInfo, RtmReleaseEntityInfo function [RAS], _rtmv2ref_rtmreleaseentityinfo, rras.rtmreleaseentityinfo, rtmv2/RtmReleaseEntityInfo
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
 - RtmReleaseEntityInfo
 - rtmv2/RtmReleaseEntityInfo
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
 - RtmReleaseEntityInfo
---

# RtmReleaseEntityInfo function


## -description

The 
<b>RtmReleaseEntityInfo</b> function releases a client structure.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EntityInfo [in]

Pointer to the handle to release. The handle was obtained with a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetentityinfo">RtmGetEntityInfo</a>.

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

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetentityinfo">RtmGetEntityInfo</a>