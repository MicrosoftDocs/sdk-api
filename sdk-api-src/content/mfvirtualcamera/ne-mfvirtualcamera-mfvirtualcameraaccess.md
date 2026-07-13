---
UID: NE:mfvirtualcamera.__MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0003
tech.root: mf
title: MFVirtualCameraAccess
ms.date: 05/17/2021
targetos: Windows
description: Specifies the access restrictions for a virtual camera.
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
 - __MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0003
 - PMFVirtualCameraAccess
 - MFVirtualCameraAccess
f1_keywords:
 - __MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0003
 - mfvirtualcamera/__MIDL___MIDL_itf_mfvirtualcamera_0000_0000_0003
 - PMFVirtualCameraAccess
 - mfvirtualcamera/PMFVirtualCameraAccess
 - MFVirtualCameraAccess
 - mfvirtualcamera/MFVirtualCameraAccess
dev_langs:
 - c++
---

## -description

Specifies the access restrictions for a virtual camera.

## -enum-fields

### -field MFVirtualCameraAccess_CurrentUser

The virtual camera can only be accessed by the current user.

### -field MFVirtualCameraAccess_AllUsers

The virtual camera can be accessed by all users.

## -remarks

Values from this enumeration are passed into [MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md). To create a virtual camera with **MFVirtualCameraAccess_AllUsers**, the caller of **MFCreateVirtualCamera** must have administrator permissions.

## -see-also

[MFCreateVirtualCamera](nf-mfvirtualcamera-mfcreatevirtualcamera.md)

