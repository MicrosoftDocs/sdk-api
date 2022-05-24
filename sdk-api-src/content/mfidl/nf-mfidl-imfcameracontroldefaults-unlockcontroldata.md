---
UID: NF:mfidl.IMFCameraControlDefaults.UnlockControlData
tech.root: mf
title: IMFCameraControlDefaults::UnlockControlData
ms.date: 05/06/2022
targetos: Windows
description: Unlocks the control data buffer unlocked with a call to LockControlData.
prerelease: false
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
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
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
 - IMFCameraControlDefaults::UnlockControlData
f1_keywords:
 - IMFCameraControlDefaults::UnlockControlData
 - mfidl/IMFCameraControlDefaults::UnlockControlData
dev_langs:
 - c++
helpviewer_keywords:
 - UnlockControlData
---

## -description

Unlocks the control data buffer unlocked with a call to [LockControlData](nf-mfidl-imfcameracontroldefaults-lockcontroldata.md).

## -returns

S_OK on success.

## -remarks

After calling **UnlockCOntrolData**, clients should not modify the contents of the control data buffer. Doing so will result in undefined behavior.

## -see-also

[LockControlData](nf-mfidl-imfcameracontroldefaults-lockcontroldata.md)


