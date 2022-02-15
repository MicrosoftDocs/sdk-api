---
UID: NF:mfvirtualcamera.IMFCameraSyncObject.Shutdown
tech.root: mf
title: IMFCameraSyncObject::Shutdown
ms.date: 05/17/2021
targetos: Windows
description: Shuts down the sync object.
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
 - IMFCameraSyncObject::Shutdown
f1_keywords:
 - IMFCameraSyncObject::Shutdown
 - mfvirtualcamera/IMFCameraSyncObject::Shutdown
dev_langs:
 - c++
---

## -description

Shuts down the [IMFCameraSyncObject](nn-mfvirtualcamera-imfcamerasyncobject.md).

## -remarks

**Shutdown** must be called on all sync objects created with calls to [IMFVirtualCamera::CreateSyncEvent](nf-mfvirtualcamera-imfvirtualcamera-createsyncevent.md) or [IMFVirtualCamera::CreateSyncSemaphore](nf-mfvirtualcamera-imfvirtualcamera-createsyncsemaphore.md).

For non-ONESHOT event or semaphore objects, **Shutdown** will unregister the event or semaphore handle with the virtual camera.

## -see-also

[IMFVirtualCamera::CreateSyncEvent](nf-mfvirtualcamera-imfvirtualcamera-createsyncevent.md)
[IMFVirtualCamera::CreateSyncSemaphore](nf-mfvirtualcamera-imfvirtualcamera-createsyncsemaphore.md)
