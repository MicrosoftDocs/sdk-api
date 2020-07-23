---
UID: NF:mfidl.IMFExtendedCameraControl.LockPayload
title: IMFExtendedCameraControl::LockPayload
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Locks the internal payload buffer contained in the capture device control to enable querying or changing the payload.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMFExtendedCameraControl::LockPayload
f1_keywords:
 - mfidl/IMFExtendedCameraControl::LockPayload
dev_langs:
 - c++
---

## -description

Locks the internal payload buffer contained in the capture device control to enable querying or changing the payload. 


## -parameters

### -param ppPayload

Receives a BYTE pointer to the buffer containing the raw payload. The caller should not free the buffer directly, but instead should call [IMFExtendedCameraControl::UnlockPayload](nf-mfidl-imfextendedcameracontrol-unlockpayload.md) to free the resources.

### -param pulPayload

Receives the size of the buffer returned in *ppPayload*.

## -returns

On success, returns S_OK.

## -remarks

## -see-also

