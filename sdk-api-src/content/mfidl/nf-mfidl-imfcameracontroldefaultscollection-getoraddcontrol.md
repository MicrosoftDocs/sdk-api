---
UID: NF:mfidl.IMFCameraControlDefaultsCollection.GetOrAddControl
tech.root: mf
title: IMFCameraControlDefaultsCollection::GetOrAddControl
ms.date: 05/06/2022
targetos: Windows
description: Adds a new custom camera control to the camera control collection.
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
 - IMFCameraControlDefaultsCollection::GetOrAddControl
f1_keywords:
 - IMFCameraControlDefaultsCollection::GetOrAddControl
 - mfidl/IMFCameraControlDefaultsCollection::GetOrAddControl
dev_langs:
 - c++
helpviewer_keywords:
 - GetOrAddControl
---

## -description

Adds a new camera control to the camera control collection.

## -parameters

### -param configType

A value from the [MF_CAMERA_CONTROL_CONFIGURATION_TYPE](ne-mfidl-mf_camera_control_configuration_type.md) specifying whether the control value must be set before streaming begins or after streaming starts.

### -param controlSet

A GUID specifying the control set to which the control belongs. If the **controlSet** is **KSPROPERTYSETID_ExtendedCameraControl** please use the dedicated [GetOrAddExtendedControl](nf-mfidl-imfcameracontroldefaultscollection-getoraddextendedcontrol.md) function.

### -param constrolId

The ID of the control to be added to the collection.

### -param controlSize

The size of the control, in bytes. This value must be greater than or equal to the size of [KSPROPERTY](/windows-hardware/drivers/stream/ksproperty-structure).

### -param dataSize

The size of the data payload for the control, in bytes.

### -param defaults

Receives a pointer to a [IMFCameraControlDefaults](nn-mfidl-imfcameracontroldefaults.md) instance representing the added control.

## -returns

An HRESULT, including the following:

| Value | Description |
|------------|-----------|
| S_OK | Success. |


## -remarks

For custom controls, *controlSet* and *controlId* are based on the custom control DDI published by the camera driver vendor. Similarly, the *controlSize* and *dataSize* are based on the DDI published by the vendor. 


## -see-also

