---
UID: NF:mfidl.IMFExtendedCameraControl.GetCapabilities
title: IMFExtendedCameraControl::GetCapabilities
ms.date: 11/4/2019
targetos: Windows
description: Queries for property capabilities supported by the capture device.
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
 - IMFExtendedCameraControl::GetCapabilities
f1_keywords:
 - IMFExtendedCameraControl::GetCapabilities
 - mfidl/IMFExtendedCameraControl::GetCapabilities
dev_langs:
 - c++
---

## -description

Queries for property capabilities supported by the capture device.



## -returns

A ULONGLONG mapping to property capabilities. Supported properties and capabilities are defined in the header file defined in ksmedia.h as constants with the naming convention **KSCAMERA_EXTENDEDPROP_**. For more information, see [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol).

## -remarks

Verify the presence of a particular capability by performing a bitwise AND operation with the return value of this function. Some drivers may require that the camera device preview be in a running state before it can determine which controls are supported. If you check whether a certain control is supported before the preview stream is running, the control may be described as unsupported (and thus unavailable) even though it is supported by the video device.

 The following example demonstrates querying support for the [KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON](/windows-hardware/drivers/stream/ksproperty-cameracontrol-extended-torchmode) capability.

```cpp
if (FAILED(m_cameraController->GetExtendedCameraControl(MF_CAPTURE_ENGINE_MEDIASOURCE,
    KSPROPERTY_CAMERACONTROL_EXTENDED_TORCHMODE,
    cameraControl.put())))
{
    // Return false to indicate that the Torch Mode control is not available.
    return false;
}

ULONGLONG capabilities = cameraControl->GetCapabilities();

// Check if the torch can be turned on.
if (capabilities & KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON)
{
    // Check if the torch is off.
    if ((cameraControl->GetFlags() & KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON) == 0)
    {
        // Torch is off. Tell the camera to turn it on.
        check_hresult(cameraControl->SetFlags(KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON));
        // Write the changed settings to the driver.
        check_hresult(cameraControl->CommitSettings());
    }
}

```

## -see-also

