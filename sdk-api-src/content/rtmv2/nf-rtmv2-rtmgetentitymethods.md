---
UID: NF:rtmv2.RtmGetEntityMethods
title: RtmGetEntityMethods function (rtmv2.h)
description: The RtmGetEntityMethods function queries the specified client to determine which methods are available for another client to invoke.
helpviewer_keywords: ["RtmGetEntityMethods","RtmGetEntityMethods function [RAS]","_rtmv2ref_rtmgetentitymethods","rras.rtmgetentitymethods","rtmv2/RtmGetEntityMethods"]
old-location: rras\rtmgetentitymethods.htm
tech.root: RRAS
ms.assetid: 186f4a55-d46b-42ab-b092-dc036b011594
ms.date: 12/05/2018
ms.keywords: RtmGetEntityMethods, RtmGetEntityMethods function [RAS], _rtmv2ref_rtmgetentitymethods, rras.rtmgetentitymethods, rtmv2/RtmGetEntityMethods
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
 - RtmGetEntityMethods
 - rtmv2/RtmGetEntityMethods
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
 - RtmGetEntityMethods
---

# RtmGetEntityMethods function


## -description

The 
<b>RtmGetEntityMethods</b> function queries the specified client to determine which methods are available for another client to invoke.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EntityHandle [in]

Handle to the client for which to obtain methods.

### -param NumMethods [in, out]

On input, <i>NumMethods</i> specifies a valid pointer to a <b>UINT</b> value. Specify zero to return the number of methods available to be exported. 




On output, <i>NumMethods</i> receives the number of methods exported by the client.

### -param ExptMethods [out]

Receives a pointer to an 
<a href="/windows/win32/api/rtmv2/nc-rtmv2-_entity_method">RTM_ENTITY_EXPORT_METHOD</a> structure that contains the set of method identifiers requested by the calling client.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer supplied is not large enough to hold all the requested information.

</td>
</tr>
</table>

## -remarks

Do not call another client's method directly, always use 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtminvokemethod">RtmInvokeMethod</a>. The routing table manager performs error checking when using 
<b>RtmInvokeMethod</b> to ensure that the client is not unregistering or already unregistered.

If ERROR_INSUFFICIENT_BUFFER is returned, there may be some data in <i>ExptMethods</i>; <i>NumMethods</i> specifies how many methods actually fit in the buffer.

When the entity handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleaseentities">RtmReleaseEntities</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/obtain-and-call-the-exported-methods-for-a-client">Obtain and Call the Exported Methods for a Client</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmblockmethods">RtmBlockMethods</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtminvokemethod">RtmInvokeMethod</a>