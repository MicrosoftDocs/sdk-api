---
UID: NN:mfidl.IMFExtendedCameraControl
title: IMFExtendedCameraControl
ms.date: 1/23/2020
targetos: Windows
description: This interface is used to configure the capture device's extended properties.
tech.root: mf
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFExtendedCameraControl
f1_keywords:
 - IMFExtendedCameraControl
 - mfidl/IMFExtendedCameraControl
dev_langs:
 - c++
---

## -description

This interface is used to configure a capture device's extended properties. Supported properties and capabilities are defined in the header file defined in ksmedia.h as constants with the naming convention **KSCAMERA_EXTENDEDPROP_**.

## -remarks

Get an instance of this interface by calling [IMFExtendedCameraController::GetExtendedCameraControl](nf-mfidl-imfextendedcameracontroller-getextendedcameracontrol.md)

### Unsupported properties

Note that some **KSCAMERA_EXTENDEDPROP_** properties are unsupported for this API. Their functionality can only be accessed by client apps through the WinRT media capture APIs.

#### KSPROPERTY_CAMERACONTROL_EXTENDED_WARMSTART

The behavior of this property is exposed through the following WinRT APIs:

- [PrepareLowLagPhotoCaptureAsync](/uwp/api/windows.media.capture.mediacapture.preparelowlagphotocaptureasync)
- [PrepareLowLagRecordToCustomSinkAsync](/uwp/api/windows.media.capture.mediacapture.preparelowlagrecordtocustomsinkasync)
- [PrepareLowLagRecordToStorageFileAsync](/uwp/api/windows.media.capture.mediacapture.preparelowlagrecordtostoragefileasync)
- [PrepareLowLagRecordToStreamAsync](/uwp/api/windows.media.capture.mediacapture.preparelowlagrecordtostreamasync)

These APIs cause the capture pipeline to be configured with the selected media type and put the driver pin is put into a paused state, which informs the driver to get the hardware resources allocated/configured for the operation.  This helps to minimize the latency by front-loading the preparation of resources. 

Note that the warm start functionality is an optional control for capture devices, so if the control is not available, the APIs above will not provide the warm start behavior. These APIs will still configure the sink side of the capture so there is some benefit to using them.

#### KSPROPERTY_CAMERACONTROL_EXTENDED_PHOTOMODE

The behavior of this property is exposed through the following WinRT APIs:

- [PrepareLowLagPhotoSequenceCaptureAsync](/uwp/api/windows.media.capture.mediacapture.preparelowlagphotosequencecaptureasync)
- [PrepareVariablePhotoSequenceCaptureAsync](/uwp/api/windows.media.capture.mediacapture.preparevariablephotosequencecaptureasync)

These APIs configure the both the capture and sink side of the pipeline and put the driver pin into the running state, capturing frames but not yet passing the frames to the pipeline.  The frames begin passing through the pipeline when the capture operation is started. 

Note that this functionality is an optional control for capture devices, so if the control is not available, the APIs above return an error.

## Examples

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

