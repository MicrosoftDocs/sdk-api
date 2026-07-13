---
UID: NE:mfvirtualcamera.__MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0002
tech.root: mf
title: MFVirtualCameraLifetime
ms.date: 05/17/2021
targetos: Windows
description: Specifies the lifetime of a virtual camera.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfvirtualcamera.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfvirtualcamera.h
api_name:
 - __MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0002
 - PMFVirtualCameraLifetime
 - MFVirtualCameraLifetime
f1_keywords:
 - __MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0002
 - mfvirtualcamera/__MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0002
 - PMFVirtualCameraLifetime
 - mfvirtualcamera/PMFVirtualCameraLifetime
 - MFVirtualCameraLifetime
 - mfvirtualcamera/MFVirtualCameraLifetime
dev_langs:
 - c++
---

## -description

Specifies the lifetime of a virtual camera.

## -enum-fields

### -field MFVirtualCameraLifetime_Session

The camera persists until the  [IMFVirtualCamera](nn-mfvirtualcamera-imfvirtualcamera.md) object is disposed or [IMFVirtualCamera::Shutdown](nf-mfvirtualcamera-imfvirtualcamera-shutdown.md) is called. Afterwards, the virtual camera will no longer be enumerable or activatable on the device.

### -field MFVirtualCameraLifetime_System

The virtual camera persists across sessions and reboots.

## -remarks

Values from this enumeration are passed into [MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md). 

## -see-also

[MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md)

