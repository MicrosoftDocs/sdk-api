---
UID: NF:mfvirtualcamera.IMFVirtualCamera.Shutdown
tech.root: mf
title: IMFVirtualCamera::Shutdown
ms.date: 05/17/2021
targetos: Windows
description: Releases all of the virtual camera's internal resources.
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
 - IMFVirtualCamera::Shutdown
f1_keywords:
 - IMFVirtualCamera::Shutdown
 - mfvirtualcamera/IMFVirtualCamera::Shutdown
dev_langs:
 - c++
---

## -description

Releases all of the virtual camera's internal resources.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |

## -remarks

When **Shutdown** is called, all objects created through the **IMFVirtualCamera** APIs will also be shutdown. This includes [IMFCameraSyncObject](nn-mfvirtualcamera-imfcamerasyncobject.md) objects obtained through calls to [IMFVirtualCamera::CreateSyncEvent](nf-mfvirtualcamera-imfvirtualcamera-createsyncevent.md) or [CreateSyncSemaphore](nf-mfvirtualcamera-imfvirtualcamera-createsyncsemaphore.md) and [IMFMediaSource](../mfidl/nn-mfidl-imfmediasource.md) objects obtained through a call to [IMFVirtualCamera::GetMediaSource](nf-mfvirtualcamera-imfvirtualcamera-getmediasource.md).  Attempts to use any object obtained from the **IMFVirtualCamera** after **Shutdown** has been called will result in an MF_E_SHUTDOWN error.

For virtual cameras created with a lifetime value of [MFVirtualCameraLifeTime_Session](ne-mfvirtualcamera-mfvirtualcameralifetime.md), when **Shutdown** is called, the virtual camera will be removed from the system.  Any application using the virtual camera will receive the device invalidated error MF_E_VIDEO_RECORDING_DEVICE_INVALIDATED.

## -see-also

[IMFMediaSource](../mfidl/nn-mfidl-imfmediasource.md)
[IMFVirtualCamera::GetMediaSource](nf-mfvirtualcamera-imfvirtualcamera-getmediasource.md)

