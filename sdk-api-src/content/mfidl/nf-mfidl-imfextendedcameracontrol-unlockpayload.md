---
UID: NF:mfidl.IMFExtendedCameraControl.UnlockPayload
title: IMFExtendedCameraControl::UnlockPayload
ms.date: 11/4/2019
targetos: Windows
description: Unlocks the raw payload contained in the capture device control.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFExtendedCameraControl::UnlockPayload
f1_keywords:
 - IMFExtendedCameraControl::UnlockPayload
 - mfidl/IMFExtendedCameraControl::UnlockPayload
dev_langs:
 - c++
---

## -description

Unlocks the raw payload contained in the capture device control.



## -returns

Returns S_OK on success.

## -remarks

Lock the payload in a capture device control by calling [IMFExtendedCameraControl::LockPayload](nf-mfidl-imfextendedcameracontrol-lockpayload.md).

## -see-also

