---
UID: NF:mfvirtualcamera.IMFVirtualCamera.GetMediaSource
tech.root: mf
title: IMFVirtualCamera::GetMediaSource
ms.date: 05/17/2021
targetos: Windows
description: Gets an IMFMediaSource that provides media data from the virtual camera.
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
 - IMFVirtualCamera::GetMediaSource
f1_keywords:
 - IMFVirtualCamera::GetMediaSource
 - mfvirtualcamera/IMFVirtualCamera::GetMediaSource
dev_langs:
 - c++
---

## -description

Gets an [IMFMediaSource](../mfidl/nn-mfidl-imfmediasource.md) that provides media data from the virtual camera.

## -parameters

### -param ppMediaSource

A shared-client **IMFMediaSource** from the virtual camera.

## -returns

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |

## -remarks

**GetMediaSource** may not be called until after [IMFVirtualCamera::Start](nf-mfvirtualcamera-imfvirtualcamera-start.md) has been successfully called. The **IMFMediaSource** returned in the *ppMediaSource* parameter is a media source that has reduced functionality.  It is internally marked as a shared client.  This media source is intended for apps to use as a local preview during virtual camera activation and configuration process.

If a full function **IMFMediaSource** is needed, the app must call [MFCreateDeviceSource](../mfidl/nf-mfidl-mfcreatedevicesource.md) using the symbolic link name returned in the **IMFAttributes** after a **IMFVirtualCamera::Start** call.  Doing so, however will result in an exclusive-control media source being created which, when activated, will lock out all other apps from using the virtual camera.

The lifetime of the **IMFMediaSource** retrieved by this method is directly tied to the lifetime of the [IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md) from which it is obtained.  If the **IMFVirtualCamera** is disposed or [IMFVirtualCamera::Shutdown](nf-mfvirtualcamera-imfvirtualcamera-shutdown.md) is called, the IMFMediaSource obtained from this method will also be shutdown.


## -see-also

[IMFVirtualCamera::Start](nf-mfvirtualcamera-imfvirtualcamera-start.md)

[MFCreateDeviceSource](../mfidl/nf-mfidl-mfcreatedevicesource.md)

[IMFVirtualCamera::Shutdown](nf-mfvirtualcamera-imfvirtualcamera-shutdown.md)