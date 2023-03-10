---
UID: NN:mfvirtualcamera.IMFVirtualCamera
tech.root: mf
title: IMFVirtualCamera
ms.date: 05/17/2021
targetos: Windows
description: Represents a virtual camera that can be plugged into the Media Foundation frame server pipeline.
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
 - IMFVirtualCamera
f1_keywords:
 - IMFVirtualCamera
 - mfvirtualcamera/IMFVirtualCamera
dev_langs:
 - c++
---

## -description

Represents a virtual camera that can be plugged into the Media Foundation frame server pipeline. This allows developers to create a user-mode software component that can be discovered and used by apps as if it was a hardware capture device.

## -remarks

Create an instance of **IMFVirtualCamera** by calling [MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md). When this interface is returned from **MFCreateVirtualCamera** for the first time, the interface represents a set of configuration options.  The caller is responsible for configuring the different settings on the virtual camera before starting the camera. Calling the [IMFVirtualCamera::Start](nf-mfvirtualcamera-imfvirtualcamera-start.md) method allows the camera to be discoverable and activatable on the device.

## -see-also

[MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md)

