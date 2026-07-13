---
UID: NN:mfidl.IMFCameraConfigurationManager
tech.root: mf
title: IMFCameraConfigurationManager
ms.date: 08/05/2022
targetos: Windows
description: The IMFCameraConfigurationManager interface can be created by calling the COM function CoCreateInstance, and passing the CLSID_CameraConfigurationManager as the CLSID parameter.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraConfigurationManager
f1_keywords:
 - IMFCameraConfigurationManager
 - mfidl/IMFCameraConfigurationManager
dev_langs:
 - c++
helpviewer_keywords:
 - IMFCameraConfigurationManager
---

## -description

## -remarks
An instance of the **IMFCameraConfigurationManager** interface can be created by calling the COM function [CoCreateInstance](../combaseapi/nf-combaseapi-cocreateinstance.md), and passing the **CLSID_CameraConfigurationManager** as the CLSID parameter.


## Examples

The following example demonstrates the use of **IMFCameraConfigurationManager** and related APIs to retrieve the default configuration of the eye gaze correction camera control.

```cpp
#include "wil/result_macros.h"

#include <mfapi.h>



HRESULT
FindDefaultConfigForEyeGazeCorrection(
    _In_ IMFActivate* cameraActivate,
    _COM_Outptr_ IMFCameraControlDefaults** ppConfig
)
{
    wil::com_ptr_nothrow<IMFCameraConfigurationManager>         factory;
    wil::com_ptr_nothrow<IMFCameraControlDefaultsCollection>    configCollection;

    *ppConfig = nullptr;

    RETURN_IF_FAILED(CoCreateInstance(CLSID_CameraConfigurationManager,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&factory)));

    /// Load the defaults, and then iterate through the available 
    /// configurations to find the eyegaze control. 
    RETURN_IF_FAILED(factory->LoadDefaults(cameraActivate, &configCollection));

    for (ULONG i = 0; i < configCollection->GetControlCount(); i++)
    {
        wil::com_ptr_nothrow<IMFCameraControlDefaults>  config;
        KSPROPERTY* ksprop = nullptr;
        ULONG                                           kspropSize = 0;
        void* data = nullptr;
        ULONG                                           dataSize = 0;

        RETURN_IF_FAILED(configCollection->GetControl(i, &config));
        RETURN_IF_FAILED(config->LockControlData((void**)&ksprop, &kspropSize, &data, &dataSize));
        RETURN_HR_IF(HRESULT_FROM_WIN32(ERROR_INVALID_DATA), kspropSize < sizeof(KSPROPERTY));
        if (ksprop->Set == KSPROPERTYSETID_ExtendedCameraControl &&
            ksprop->Id == KSPROPERTY_CAMERACONTROL_EXTENDED_EYEGAZECORRECTION)
        {
            (void)config->UnlockControlData();
            *ppConfig = config.detach();
            return S_OK;
        }
        (void)config->UnlockControlData();
    }

    /// If we reach this point, we didn't find the eyegaze
    /// correction control.
    return MF_E_NOT_FOUND;
}
```

The following example demostrates the use of **IMFCameraConfigurationManager** and related APIs to set the default value for the legacy exposure control. A typical usage scenario for this implementation allowing the user to set default control values in an IHV-implemented camera companion app rather than needing to launch the general Windows camera settings page.

```cpp
HRESULT SetDefaultLegacyExposure(
    _In_z_ LPCWSTR deviceSymbolicName,
    _In_ LONG exposureValue
)
{
    wil::com_ptr_nothrow<IMFAttributes> attrib;
    wil::com_ptr_nothrow<IMFCameraConfigurationManager> manager;
    wil::com_ptr_nothrow<IMFCameraControlDefaultsCollection> defaultsCollection;
    wil::com_ptr_nothrow<IMFCameraControlDefaults> exposureDefaults;
    KSPROPERTY_CAMERACONTROL_S* data = nullptr;
    ULONG dataSize = 0;
    KSPROPERTY_CAMERACONTROL_S* control = nullptr;
    ULONG controlSize = 0;
    LONG value = 0;
    MF_CAMERA_CONTROL_RANGE_INFO rangeInfo = { };
    bool fLocked = false;
    auto cleanUpOnExit = wil::scope_exit([&]()
    {
        if (fLocked)
        {
            /// Best effort to avoid leaving the control in a locked state.
            (void)exposureDefaults->UnlockControlData();
        }
        /// Free up the manager's resources when we're done.
        if (manager)
        {
            manager->Shutdown();
        }
    });

    RETURN_IF_FAILED(CoCreateInstance(CLSID_CameraConfigurationManager,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&manager)));
    RETURN_IF_FAILED(MFCreateAttributes(&attrib, 1));
    RETURN_IF_FAILED(attrib->SetString(MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            deviceSymbolicName));
    RETURN_IF_FAILED(manager->LoadDefaults(attrib.get(), &defaultsCollection));
    /// If the legacy exposure control not available, this call will 
    /// return HRESULT_FROM_WIN32(ERROR_SET_NOT_FOUND). 
    /// 
    /// Exposure control is always a post-start control since the
    /// algorithm requires frames to be captured/analyzed for the 
    /// exposure to converge.
    RETURN_IF_FAILED(defaultsCollection->GetOrAddControl(MF_CAMERA_CONTROL_CONFIGURATION_TYPE_POSTSTART,
        PROPSETID_VIDCAP_CAMERACONTROL,

        KSPROPERTY_CAMERACONTROL_EXPOSURE,

        sizeof(KSPROPERTY_CAMERACONTROL_S),
        sizeof(KSPROPERTY_CAMERACONTROL_S),
        &exposureDefaults));
    /// Exposure off the PROPSETID_VIDCAP_CAMERACONTROL must always
    /// provide a min/max/step/default. We can validate the 
    /// parameter provided is valid. 
    /// NOTE: RangeInfo is only guaranteed for 
    /// PROPSETID_VIDCAP_CAMERACONTROL or 
    /// PROPSETID_VIDCAP_VIDEOPROCAMP. Other controls may provide 
    /// range information (they must support 
    /// KSPROPERTY_TYPE_BASICSUPPORT operation), but the app must 
    /// handle the situation where range information may not be 
    /// available. 
    RETURN_IF_FAILED(exposureDefaults->GetRangeInfo(&rangeInfo));
    if ((rangeInfo.minValue > exposureValue) ||
        (rangeInfo.maxValue < exposureValue) ||
        (0 != (exposureValue - rangeInfo.minValue) % rangeInfo.stepValue))
    {
        RETURN_IF_FAILED(E_INVALIDARG);
    }

    /// Since we're setting a specific value, we need to also check
    /// 1. Does this control support manual mode (most webcam do,
    /// but per DDI spec, not required).
    /// 2. Flip the flags to manual mode so the camera won't ignore
     /// the new value being set.
    RETURN_IF_FAILED(exposureDefaults->LockControlData((void**)&control,
        &controlSize,
        (void**)&data,
        &dataSize));
    fLocked = true;
    if (controlSize < sizeof(KSPROPERTY_CAMERACONTROL_S) ||
        dataSize < sizeof(KSPROPERTY_CAMERACONTROL_S))
    {
        /// This should never happen, but just to keep everything sane.
        RETURN_IF_FAILED(MF_E_UNEXPECTED);
    }
    if (WI_IsFlagClear(control->Capabilities, KSPROPERTY_CAMERACONTROL_FLAGS_MANUAL))
    {
        RETURN_IF_FAILED(HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED));
    }
    control->Flags = KSPROPERTY_CAMERACONTROL_FLAGS_MANUAL;
    control->Property.Flags = KSPROPERTY_TYPE_SET;
    control->Value = exposureValue;
    /// For legacy control, we send in the same information in the 
    /// data as the control. 
    data->Property.Set = control->Property.Set;

    data->Property.Id = control->Property.Id;
    data->Property.Flags = control->Property.Flags;
    data->Value = control->Value;
    data->Flags = control->Flags;
    RETURN_IF_FAILED(exposureDefaults->UnlockControlData());
    fLocked = false;
    RETURN_IF_FAILED(manager->SaveDefaults(defaultsCollection.get()));
    return S_OK;
}
```

The following example illustrates another scenario where IHVs implement their own configuration applications providing the user with a UX to configure custom controls. In this scenario, the IHV app has found the front facing camera (FFC) which supports a custom control and the IHV chose to have the camera in question always default to the KSCAMERAPROFILE_VideoConferencing profile unless the application explicitly overrides this behavior by selecting a different profile. Because custom controls have control and data payload schemas which are unknown to Windows and only known to the IHV/OEMs and/or ISVs who obtained the specifications for the custom control, the sample below does not show any validation of the control or data payload.

```cpp
HRESULT SetCustomControl(
    _In_ IMFAttributes* attribFrontFacingCamera,
    _In_ REFGUID customSet,
    _In_ ULONG customId,
    _In_reads_bytes_(customDataSize) void* customData,
    _In_ ULONG customDataSize)
{
    wil::com_ptr_nothrow<IMFCameraConfigurationManager> manager;
    wil::com_ptr_nothrow<IMFCameraControlDefaultsCollection> defaultsCollection;
    wil::com_ptr_nothrow<IMFCameraControlDefaults> customControlDefaults;
    BYTE* data = nullptr;
    ULONG dataSize = 0;
    KSPROPERTY* control = nullptr;
    ULONG controlSize = 0;
    LONG value = 0;
    MF_CAMERA_CONTROL_RANGE_INFO rangeInfo = { };
    bool fLocked = false;
    auto cleanUpOnExit = wil::scope_exit([&]()
    {
        if (fLocked)
        {
            /// Best effort to avoid leaving the control in a locked state.
            (void)customControlDefaults->UnlockControlData();
        }
        /// Free up the manager's resources when we're done.
        if (manager)
        {
            manager->Shutdown();
        }
    });

    RETURN_IF_FAILED(CoCreateInstance(CLSID_CameraConfigurationManager, nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&manager)));
    RETURN_IF_FAILED(manager->LoadDefaults(attribFrontFacingCamera, &defaultsCollection));
    /// Set the selected profile to the video conferencing profile. 
    /// This is making the assumption that the most common use of 
    /// the front facing camera would be for video conferencing 
    /// calls, but for apps like CameraApp, they can (and do) 
    /// override this selection by explicitly setting a different 
    /// profile (either Photo or Video Recording) as needed. 
    /// 
    /// NOTE: As this is done by the IHV/OEM (who also publishes 
    /// the camera profiles), the assumption is that there's 
    /// knowledge of the camera's support for the video conferencing 
    /// profile and the index value for that profile (profiles are 
    /// identified by their type such as 
    /// KSCAMERAPROFILE_VideoConferencing and their index which 
    /// allows for multiple profiles for the same "type"). 
    RETURN_IF_FAILED(defaultsCollection->SetGUID(MF_CAPTURE_ENGINE_SELECTEDCAMERAPROFILE,
        KSCAMERAPROFILE_VideoConferencing));
    RETURN_IF_FAILED(defaultsCollection -> SetUINT32(MF_CAPTURE_ENGINE_SELECTEDCAMERAPROFILE_INDEX,
            0));
    /// Custom controls are never validated, it is assumed the
    /// caller of this method has some out of band knowledge of the
    /// DDI's control/data schema. This is typically done by IHVs
    /// documenting their controls for ISVs/OEMs to leverage.

    RETURN_IF_FAILED (defaultsCollection->GetOrAddControl(MF_CAMERA_CONTROL_CONFIGURATION_TYPE_POSTSTART,
        customSet,
        customId,
        sizeof(KSPROPERTY),
        customDataSize,
        &customControlDefaults));
        RETURN_IF_FAILED(customControlDefaults->LockControlData((void**)&control,
            &controlSize,
            (void**)&data,
            &dataSize));
        fLocked = true;
        if (controlSize < sizeof(KSPROPERTY) || dataSize < customDataSize)
        {
            /// This should never happen, but just to keep everything sane.
            RETURN_IF_FAILED(MF_E_UNEXPECTED);
        }
        control->Set = customSet;
        control->Id = customId;
        control->Flags = KSPROPERTY_TYPE_SET;
        CopyMemory(data, customData, customDataSize);
        RETURN_IF_FAILED(customControlDefaults->UnlockControlData());
        fLocked = false;
        RETURN_IF_FAILED(manager->SaveDefaults(defaultsCollection.get()));
        return S_OK;
}
```

## -see-also

