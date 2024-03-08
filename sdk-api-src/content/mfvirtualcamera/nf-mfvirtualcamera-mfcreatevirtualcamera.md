---
UID: NF:mfvirtualcamera.MFCreateVirtualCamera
tech.root: mf
title: MFCreateVirtualCamera
ms.date: 05/17/2021
targetos: Windows
description: Creates a virtual camera object which can be used by the caller to register, unregister, or remove the virtual camera from the system.
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
 - MFCreateVirtualCamera
f1_keywords:
 - MFCreateVirtualCamera
 - mfvirtualcamera/MFCreateVirtualCamera
dev_langs:
 - c++
---

## -description

Creates a virtual camera object which can be used by the caller to register, unregister, or remove the virtual camera from the system.

## -parameters

### -param type

A member of the [MFVirtualCameraType](ne-mfvirtualcamera-mfvirtualcameratype.md) enumeration specifying the virtual camera type. In the current release, only **MFVirtualCameraType_SoftwareCameraSource** is supported.

### -param lifetime

A member of the [MFVirtualCameraLifetime](ne-mfvirtualcamera-mfvirtualcameralifetime.md) enumeration specifying the lifetime of the camera. If **MFVirtualCameraLifetime_Session** is specified, when the returned [IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md) object is disposed or [IMFVirtualCamera::Shutdown](nf-mfvirtualcamera-imfvirtualcamera-shutdown.md) is called, the virtual camera will no longer be enumerable or activatable on the device.  If you want the virtual camera to persist across sessions and/or across reboots, you must specify the value **MFVirtualCameraLifetime_System**.

### -param access

A member of the [MFVirtualCameraAccess](ne-mfvirtualcamera-mfvirtualcameraaccess.md) enumeration specifying the access scope of the created virtual camera. If **MFVirtualCameraAccess_CurrentUser** is specified, the virtual camera is only created for the user account that called the **MFCreateVirtualCamera**.  If **MFVirtualCameraAccess_AllUsers** is specified, all users on the device will be able to enumerate or activate the virtual camera.  To create a virtual camera with **MFVirtualCameraAccess_AllUsers**, the caller of **MFCreateVirtualCamera** must have administrator permissions.

### -param friendlyName

A null-terminated, user-readable Unicode string friendly name for the created virtual camera.  The pipeline will automatically append “Windows Virtual Camera” to the provided friendly name to ensure end users can distinguish virtual cameras from physical cameras based on the friendly name.  This parameter must not be nullptr.

### -param sourceId

The unique CLSID of the custom media source to be activated for this virtual camera.  The string must be in the “{CLSID}” format.  This parameter must not be nullptr.

### -param categories

An optional list of device interface categories under which the virtual camera is registered.  If a non-administrator user is invoking **MFCreateVirtualCamera**, the categories must be a subset of the following values:
 
- [KSCATEGORY_VIDEO_CAMERA](/windows-hardware/drivers/install/kscategory-video-camera)
- [KSCATEGORY_VIDEO](/windows-hardware/drivers/install/kscategory-video)
- [KSCATEGORY_CAPTURE](/windows-hardware/drivers/install/kscategory-capture)
- [KSCATEGORY_SENSOR_CAMERA](/windows-hardware/drivers/install/kscategory-sensor-camera)

If nullptr is specified, the virtual camera is registered under the KSCATEGORY_VIDEO_CAMERA, KSCATEGORY_VIDEO and KSCATEGORY_CAPTURE categories.

### -param categoryCount

The number of categories provided in the *categories* parameter.  If *categories* is nullptr, *categoryCount* must be 0.

### -param virtualCamera

Output parameter that receives the newly created [IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md).  This parameter must not be nullptr.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG | An input parameter is invalid. |
| E_POINTER | The *virtualCamera* parameter is nullptr. |
| E_ACCESSDENIED | Privacy control is set to deny access to the camera for the app, user, or system.  Or the caller is not an administrator and the parameters provided are only valid for administrator access.  |



## -remarks

The virtual camera created by **MFCreateVirtualCamera** is keyed off the parameters passed in to this API.  By keeping the same parameters, applications can re-open the same virtual camera. When called for the first time, the resulting [IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md) contains a set of configuration information which may be modified or updated by the caller to create a new instance of a virtual camera.  If the same parameters are used for this function on subsequent calls, the resulting **IMFVirtualCamera** will open the existing virtual camera when the [IMFVirtualCamera::Start](nf-mfvirtualcamera-imfvirtualcamera-start.md) or [IMFVirtualCamera::Stop](nf-mfvirtualcamera-imfvirtualcamera-stop.md) method is called. Calling [IMFVirtualCamera::Remove](nf-mfvirtualcamera-imfvirtualcamera-remove.md) will remove the existing virtual camera. If MFVirtualCameraAccess_CurrentUser is specified for the *access* parameter, each user account gets a unique virtual camera.

UWP and Packaged Application must declare the *webcam* device capability in their manifest in order to use this API. This API is also subject to the webcam privacy control so when privacy is set to deny access, this API will result in an E_ACCESSDENIED failure.

> [!NOTE]
> UWP and Packaged Apps must not invoke **MFCreateVirtualCamera** on their UI thread.  Doing so will potentially trigger a deadlock as the Capability Access Manager check for the webcam access consent dialog will be blocked.



## -see-also

[IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md)
[MFVirtualCameraType](ne-mfvirtualcamera-mfvirtualcameratype.md)
[MFVirtualCameraLifetime](ne-mfvirtualcamera-mfvirtualcameralifetime.md)
[MFVirtualCameraAccess](ne-mfvirtualcamera-mfvirtualcameraaccess.md)

