---
UID: NF:rtmv2.RtmGetEntityInfo
title: RtmGetEntityInfo function (rtmv2.h)
description: The RtmGetEntityInfo function returns information about a previously registered client.
helpviewer_keywords: ["RtmGetEntityInfo","RtmGetEntityInfo function [RAS]","_rtmv2ref_rtmgetentityinfo","rras.rtmgetentityinfo","rtmv2/RtmGetEntityInfo"]
old-location: rras\rtmgetentityinfo.htm
tech.root: RRAS
ms.assetid: 6062369c-22c7-48e4-9dd3-91efba22df34
ms.date: 12/05/2018
ms.keywords: RtmGetEntityInfo, RtmGetEntityInfo function [RAS], _rtmv2ref_rtmgetentityinfo, rras.rtmgetentityinfo, rtmv2/RtmGetEntityInfo
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
 - RtmGetEntityInfo
 - rtmv2/RtmGetEntityInfo
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
 - RtmGetEntityInfo
---

# RtmGetEntityInfo function


## -description

The 
<b>RtmGetEntityInfo</b> function returns information about a previously registered client.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EntityHandle [in]

Handle to the client for which to return information.

### -param EntityInfo [out]

On input, <i>EntityInfo</i> is a pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a> structure. 




On output, <i>EntityInfo</i> receives the requested information.

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



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentityinfo">RtmReleaseEntityInfo</a>