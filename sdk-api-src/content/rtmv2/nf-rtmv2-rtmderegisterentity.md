---
UID: NF:rtmv2.RtmDeregisterEntity
title: RtmDeregisterEntity function (rtmv2.h)
description: The RtmDeregisterEntity function unregisters a client from a routing table manager instance and address family.
helpviewer_keywords: ["RtmDeregisterEntity","RtmDeregisterEntity function [RAS]","_rtmv2ref_rtmderegisterentity","rras.rtmderegisterentity","rtmv2/RtmDeregisterEntity"]
old-location: rras\rtmderegisterentity.htm
tech.root: RRAS
ms.assetid: dc13022b-e474-4442-a19c-856ee130c383
ms.date: 12/05/2018
ms.keywords: RtmDeregisterEntity, RtmDeregisterEntity function [RAS], _rtmv2ref_rtmderegisterentity, rras.rtmderegisterentity, rtmv2/RtmDeregisterEntity
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
 - RtmDeregisterEntity
 - rtmv2/RtmDeregisterEntity
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
 - RtmDeregisterEntity
---

# RtmDeregisterEntity function


## -description

The 
<b>RtmDeregisterEntity</b> function unregisters a client from a routing table manager instance and address family.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

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

Before calling this function, the client must ensure that all locks, handles, and information structures are released with the appropriate functions.

When the client calls 
<b>RtmDeregisterEntity</b>, the handle that was returned by a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a> is released. The client must not call any RTMv2 functions after releasing this handle.

If the client does call any functions that access the routing table manager after the client has unregistered, the client's process may be terminated.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>