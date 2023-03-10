---
UID: NF:mfidl.IMFExtendedCameraControl.GetFlags
title: IMFExtendedCameraControl::GetFlags
ms.date: 11/4/2019
targetos: Windows
description: Queries for property flags on the capture device.
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
 - IMFExtendedCameraControl::GetFlags
f1_keywords:
 - IMFExtendedCameraControl::GetFlags
 - mfidl/IMFExtendedCameraControl::GetFlags
dev_langs:
 - c++
---

## -description

Queries for property flags on the capture device.



## -returns

A ULONGLONG mapping to property flags. Supported properties and flags are defined in the header file defined in ksmedia.h as constants with the naming convention **KSCAMERA_EXTENDEDPROP_**. For more information, see [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol).

## -remarks

Set the property flags on the capture device by calling [IMFExtendedCameraControl::SetFlags](nf-mfidl-imfextendedcameracontrol-setflags.md). Before setting a property flag, you can check for supported capabilities by calling [IMFExtendedCameraControl::GetCapabilities](nf-mfidl-imfextendedcameracontrol-getcapabilities.md). The following example demonstrates querying support for the [KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON](/windows-hardware/drivers/stream/ksproperty-cameracontrol-extended-torchmode) capability.

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

