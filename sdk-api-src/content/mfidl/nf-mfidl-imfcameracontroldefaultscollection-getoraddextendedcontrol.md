---
UID: NF:mfidl.IMFCameraControlDefaultsCollection.GetOrAddExtendedControl
tech.root: mf
title: IMFCameraControlDefaultsCollection::GetOrAddExtendedControl
ms.date: 05/06/2022
targetos: Windows
description: Adds a new extended camera control to the camera control collection.
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
 - IMFCameraControlDefaultsCollection::GetOrAddExtendedControl
f1_keywords:
 - IMFCameraControlDefaultsCollection::GetOrAddExtendedControl
 - mfidl/IMFCameraControlDefaultsCollection::GetOrAddExtendedControl
dev_langs:
 - c++
helpviewer_keywords:
 - GetOrAddExtendedControl
---

## -description

Adds a new extended camera control to the camera control collection.

## -parameters

### -param configType [in]

A value from the [MF_CAMERA_CONTROL_CONFIGURATION_TYPE](ne-mfidl-mf_camera_control_configuration_type.md) specifying whether the control value must be set before streaming begins or after streaming starts.

### -param constrolId [in]

The ID of the control to be added to the collection. This value must be an ID  in the [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol) property set.

### -param streamId [in]

The ID of the stream associated with the control. This paramater is only used for pin-level controls. Otherwise, this value is ignored.

### -param dataSize [in]

The size of the data payload for the control, in bytes.

### -param defaults [out]

Receives a pointer to a [IMFCameraControlDefaults](nn-mfidl-imfcameracontroldefaults.md) instance representing the added control.

## -returns

An HRESULT, including the following:

| Value | Description |
|------------|-----------|
| S_OK | Success. |
| MF_E_INVALIDREQUEST | The specified control ID is not in the KSPROPERTYSETID_ExtendedCameraControl property set. |

## -remarks

The data payload size may vary for different controls. The *dataSize* value must be valid for the control payload schema so the control can reserve the buffer required. 

## -see-also

