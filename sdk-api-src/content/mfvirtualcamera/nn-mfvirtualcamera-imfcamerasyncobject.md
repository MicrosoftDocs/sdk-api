---
UID: NN:mfvirtualcamera.IMFCameraSyncObject
tech.root: mf
title: IMFCameraSyncObject
ms.date: 05/17/2021
targetos: Windows
description: Provides a synchronization mechanism between an app that creates and manages a virtual camera and the virtual camera source.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFCameraSyncObject
f1_keywords:
 - IMFCameraSyncObject
 - mfvirtualcamera/IMFCameraSyncObject
dev_langs:
 - c++
---

## -description

Provides a synchronization mechanism between an app that creates and manages a virtual camera and the virtual camera source.

## -remarks

Get an instance of this interface by calling [IMFVirtualCamera::CreateSyncEvent](nf-mfvirtualcamera-imfvirtualcamera-createsyncevent.md) or [IMFVirtualCamera::CreateSyncSemaphore](nf-mfvirtualcamera-imfvirtualcamera-createsyncsemaphore.md).

## -see-also

[IMFVirtualCamera::CreateSyncEvent](nf-mfvirtualcamera-imfvirtualcamera-createsyncevent.md) [IMFVirtualCamera::CreateSyncSemaphore](nf-mfvirtualcamera-imfvirtualcamera-createsyncsemaphore.md)

