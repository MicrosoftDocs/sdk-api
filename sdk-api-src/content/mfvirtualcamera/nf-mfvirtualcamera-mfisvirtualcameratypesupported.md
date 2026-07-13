---
UID: NF:mfvirtualcamera.MFIsVirtualCameraTypeSupported
tech.root: mf
title: MFIsVirtualCameraTypeSupported
ms.date: 05/17/2021
targetos: Windows
description: Returns a value indicating if a particular virtual camera is supported on the platform.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfsensorgroup.dll
api_name:
 - MFIsVirtualCameraTypeSupported
f1_keywords:
 - MFIsVirtualCameraTypeSupported
 - mfvirtualcamera/MFIsVirtualCameraTypeSupported
dev_langs:
 - c++
---

## -description

Returns a value indicating if a particular virtual camera is supported on the current device.

## -parameters

### -param type

A member of the [MFVirtualCameraType](ne-mfvirtualcamera-mfvirtualcameratype.md) enumeration specifying the virtual camera type for which support is being queried. In the current release, only **MFVirtualCameraType_SoftwareCameraSource** is supported.

### -param supported

An output parameter that receives a boolean indicating if the specified camera type is supported on the current device.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG | An input parameter is invalid. |
| E_POINTER | The *supported* parameter is nullptr. |
| E_ACCESSDENIED | Privacy control is set to deny access to the camera for the app, user, or system.  Or the caller is not an administrator and the parameters provided are only valid for administrator access.  |


## -remarks

## -see-also

[MFVirtualCameraType](ne-mfvirtualcamera-mfvirtualcameratype.md)

