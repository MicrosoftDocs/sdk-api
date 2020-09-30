---
UID: NF:rtmv2.RtmGetOpaqueInformationPointer
title: RtmGetOpaqueInformationPointer function (rtmv2.h)
description: The RtmGetOpaqueInformationPointer function returns a pointer to the opaque information field in a destination that is reserved for this client.
helpviewer_keywords: ["RtmGetOpaqueInformationPointer","RtmGetOpaqueInformationPointer function [RAS]","_rtmv2ref_rtmgetopaqueinformationpointer","rras.rtmgetopaqueinformationpointer","rtmv2/RtmGetOpaqueInformationPointer"]
old-location: rras\rtmgetopaqueinformationpointer.htm
tech.root: RRAS
ms.assetid: 7ad948fa-cd00-4496-bd62-433d7faa0f85
ms.date: 12/05/2018
ms.keywords: RtmGetOpaqueInformationPointer, RtmGetOpaqueInformationPointer function [RAS], _rtmv2ref_rtmgetopaqueinformationpointer, rras.rtmgetopaqueinformationpointer, rtmv2/RtmGetOpaqueInformationPointer
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
 - RtmGetOpaqueInformationPointer
 - rtmv2/RtmGetOpaqueInformationPointer
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
 - RtmGetOpaqueInformationPointer
---

# RtmGetOpaqueInformationPointer function


## -description

The 
<b>RtmGetOpaqueInformationPointer</b> function returns a pointer to the opaque information field in a destination that is reserved for this client. The pointer enables the client to store client-specific information with the destination in the routing table.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestHandle [in]

Handle to the destination.

### -param OpaqueInfoPointer [out]

On input, <i>OpaqueInfoPointer</i> is a pointer to <b>NULL</b>. 




On output, <i>OpaqueInfoPointer</i> receives a pointer to the opaque information pointer. If a client has not reserved an opaque pointer during registration, this parameter remains unchanged.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No opaque pointer was reserved by the client.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

For sample code using this function, see 
<a href="/windows/desktop/RRAS/access-the-opaque-pointer-in-a-destination">Access the Opaque Pointer in a Destination</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmlockdestination">RtmLockDestination</a>