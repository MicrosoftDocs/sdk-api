---
UID: NF:rtmv2.RtmGetRegisteredEntities
title: RtmGetRegisteredEntities function (rtmv2.h)
description: The RtmGetRegisteredEntities function returns information about all clients that have registered with the specified instance of the routing table manager and specified address family.
helpviewer_keywords: ["RtmGetRegisteredEntities","RtmGetRegisteredEntities function [RAS]","_rtmv2ref_rtmgetregisteredentities","rras.rtmgetregisteredentities","rtmv2/RtmGetRegisteredEntities"]
old-location: rras\rtmgetregisteredentities.htm
tech.root: RRAS
ms.assetid: 411e15bc-7f47-4ef7-9400-292203b581af
ms.date: 12/05/2018
ms.keywords: RtmGetRegisteredEntities, RtmGetRegisteredEntities function [RAS], _rtmv2ref_rtmgetregisteredentities, rras.rtmgetregisteredentities, rtmv2/RtmGetRegisteredEntities
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
 - RtmGetRegisteredEntities
 - rtmv2/RtmGetRegisteredEntities
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
 - RtmGetRegisteredEntities
---

# RtmGetRegisteredEntities function


## -description

The 
<b>RtmGetRegisteredEntities</b> function returns information about all clients that have registered with the specified instance of the routing table manager and specified address family.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param NumEntities [in, out]

On input, <i>NumEntities</i> is a pointer to a <b>UINT</b> value, which specifies the maximum number of clients that can be received by <i>EntityInfos</i>. On output, <i>NumEntities</i> receives the actual number of clients received by <i>EntityInfos</i>.

### -param EntityHandles [out]

If handles must be returned: On input, <i>EntityHandles</i> is a pointer to <b>NULL</b>. On output, <i>EntityHandles</i> receives a pointer to an array of entity handle; otherwise, <i>EntityHandles</i> remains unchanged. 




If handles do not need to be returned: On input, <i>EntityHandles</i> is <b>NULL</b>.

### -param EntityInfos [out]

If a pointer must be returned: On input, <i>EntityInfos</i> is a pointer to <b>NULL</b>. On output, <i>EntityInfos</i> receives a pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a> structures; otherwise, <i>EntityInfos</i> remains unchanged. 




If a pointer does not need to be returned: On input, <i>EntityInfos</i> is <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer supplied is not large enough to hold all the requested information.

</td>
</tr>
</table>

## -remarks

If <b>ERROR_INSUFFICIENT_BUFFER</b> is returned, there may be some data in <i>EntityHandles</i>. The <i>NumEntities</i> parameter specifies how many entities were actually returned.

The 
<b>RtmGetRegisteredEntities</b> function can be used by routing protocols to verify which other protocols are running for that address family and routing table manager instance. Based on the information returned, a client can then perform protocol-specific processing.

The RTMv2 API supports only one instance of the routing table manager.

When the entities are no longer required, release them by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentities">RtmReleaseEntities</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/enumerate-the-registered-entities">Enumerate the Registered Entities</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentities">RtmReleaseEntities</a>