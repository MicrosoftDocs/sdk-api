---
UID: NF:mfidl.IMFCameraControlDefaults.LockControlData
tech.root: mf
title: IMFCameraControlDefaults::LockControlData
ms.date: 05/06/2022
targetos: Windows
description: Retrieves the data payload for the control associated with the IMFCameraControlDefaults instance, allowing clients to modify the control value directly.
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
 - IMFCameraControlDefaults::LockControlData
f1_keywords:
 - IMFCameraControlDefaults::LockControlData
 - mfidl/IMFCameraControlDefaults::LockControlData
dev_langs:
 - c++
helpviewer_keywords:
 - LockControlData
---

## -description

Retrieves the data payload for the control associated with the **IMFCameraControlDefaults** instance, allowing clients to modify the control value directly.

## -parameters

### -param control [out]

Receives a pointer to the control being locked.

### -param controlSize [out]

Receives the size of the structure pointed to by *control*.

### -param data [out]

Receives a pointer to the data payload of the control. 

### -param dataSize [out]

Receives the size of the buffer pointed to by *dataSize*. 

## -returns

S_OK on success.

## -remarks

The *control* and *data* parameters are not type checked because custom controls can have arbitrary payload schema sizes.

You must call [UnlockControlData](nf-mfidl-imfcameracontroldefaults-unlockcontroldata.md) must be called before the collection containing the control is submitted to [IMFCameraConfigurationManager::SaveDefaults](nf-mfidl-imfcameraconfigurationmanager-savedefaults.md) method.


## -see-also

[UnlockControlData](nf-mfidl-imfcameracontroldefaults-unlockcontroldata.md)

[IMFCameraConfigurationManager::SaveDefaults](nf-mfidl-imfcameraconfigurationmanager-savedefaults.md)

