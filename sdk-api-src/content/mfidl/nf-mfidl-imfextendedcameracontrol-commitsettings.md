---
UID: NF:mfidl.IMFExtendedCameraControl.CommitSettings
title: IMFExtendedCameraControl::CommitSettings
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Commits the configured control settings to the camera driver. 
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
 - IMFExtendedCameraControl::CommitSettings
f1_keywords:
 - mfidl/IMFExtendedCameraControl::CommitSettings
dev_langs:
 - c++
---

## -description

Commits the configured control settings to the camera driver. 

## -returns

Returns S_OK on success. 

## -remarks

The following example demonstrates setting the [KSCAMERA_EXTENDEDPROP_VIDEOTORCH_ON](/windows-hardware/drivers/stream/ksproperty-cameracontrol-extended-torchmode) flag and committing the setting.

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

