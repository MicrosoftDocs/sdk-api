---
UID: NF:rtmv2.RtmLockDestination
title: RtmLockDestination function (rtmv2.h)
description: The RtmLockDestination function locks or unlocks a destination in the routing table. Use this function to protect a destination while changing opaque pointers.
helpviewer_keywords: ["RtmLockDestination","RtmLockDestination function [RAS]","_rtmv2ref_rtmlockdestination","rras.rtmlockdestination","rtmv2/RtmLockDestination"]
old-location: rras\rtmlockdestination.htm
tech.root: RRAS
ms.assetid: 5666dc47-811f-481e-8bda-bf814a4028de
ms.date: 12/05/2018
ms.keywords: RtmLockDestination, RtmLockDestination function [RAS], _rtmv2ref_rtmlockdestination, rras.rtmlockdestination, rtmv2/RtmLockDestination
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
 - RtmLockDestination
 - rtmv2/RtmLockDestination
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
 - RtmLockDestination
---

# RtmLockDestination function


## -description

The 
<b>RtmLockDestination</b> function locks or unlocks a destination in the routing table. Use this function to protect a destination while changing opaque pointers.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param DestHandle [in]

Handle to the destination to lock.

### -param Exclusive [in]

Specifies whether to lock or unlock the destination in an exclusive (<b>TRUE</b>) or shared (<b>FALSE</b>) mode.

### -param LockDest [in]

Specifies whether to lock or unlock the destination. Specify <b>TRUE</b> to lock the destination; specify <b>FALSE</b> to unlock it.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling client does not own this destination.

</td>
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

This function also locks the associated routes. Avoid locking destinations for long periods of time, because no other client can access the destination and associated routes until the lock is released.

A client can also use this function when reading information for a destination, while preventing changes during the client's read operation. In this case, consider using 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetdestinfo">RtmGetDestInfo</a> instead.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/update-a-route-in-place-using-rtmupdateandunlockroute">Update a Route In Place Using RtmUpdateAndUnlockRoute</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer">RtmGetOpaqueInformationPointer</a>