---
UID: NF:mfvirtualcamera.IMFVirtualCamera.AddDeviceSourceInfo
tech.root: mf
title: IMFVirtualCamera::AddDeviceSourceInfo
ms.date: 05/17/2021
targetos: Windows
description: Informs the pipeline the virtual camera will require exclusive control to the physical camera specified by the specified device symbolic name.
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
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFVirtualCamera::AddDeviceSourceInfo
f1_keywords:
 - IMFVirtualCamera::AddDeviceSourceInfo
 - mfvirtualcamera/IMFVirtualCamera::AddDeviceSourceInfo
dev_langs:
 - c++
---

## -description

Informs the pipeline the virtual camera will require exclusive control to the physical camera specified by the specified device symbolic name.  

## -parameters

### -param DeviceSourceInfo

A **LPCWSTR** containing the symbolic name for the physical camera. This value is enumerated through the standard Windows enumeration APIs such as [MFEnumDeviceSources](../mfidl/nf-mfidl-mfenumdevicesources.md) and [DeviceInformation](/uwp/api/Windows.Devices.Enumeration.DeviceInformation)

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG | An input parameter is invalid. |

## -remarks

The function allows the Windows Camera Frame Server service to arbitrate access to the physical camera when the virtual camera is activated.

This API may be called repeatedly if the virtual camera requires exclusive access to more than one physical camera.

> [!NOTE]
> When the virtual camera is activated all physical cameras added to the virtual camera using this API will be marked as in use.  So any attempt to access those physical cameras in non-shared mode will result in a sharing violation.


## -see-also

[MFEnumDeviceSources](../mfidl/nf-mfidl-mfenumdevicesources)
[DeviceInformation](/uwp/api/Windows.Devices.Enumeration.DeviceInformation)

