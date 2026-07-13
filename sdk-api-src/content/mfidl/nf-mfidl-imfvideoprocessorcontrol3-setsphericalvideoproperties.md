---
UID: NF:mfidl.IMFVideoProcessorControl3.SetSphericalVideoProperties
tech.root: mf
title: IMFVideoProcessorControl3::SetSphericalVideoProperties
ms.date: 09/09/2025
targetos: Windows
description: When rendering spherical video (360 video) this sets the view direction of the camera.  X,Y,Z,W are the components of the camera's view direction quaternion.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1803
req.target-min-winversvr: Windows Server version 1803
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl3::SetSphericalVideoProperties
f1_keywords:
 - IMFVideoProcessorControl3::SetSphericalVideoProperties
 - mfidl/IMFVideoProcessorControl3::SetSphericalVideoProperties
dev_langs:
 - c++
helpviewer_keywords:
 - SetSphericalVideoProperties
---

## -description

When rendering spherical video (360 video) this sets the view direction of the camera.  X,Y,Z,W are the components of the camera's view direction quaternion.


## -parameters

### -param X [in]

The X component of view direction quaternion.

### -param Y [in]

The Y component of view direction quaternion.

### -param Z [in]

The Z component of view direction quaternion.

### -param W [in]

The W component of view direction quaternion.

### -param fieldOfView [in]

A DWORD specifying the field of view, in degrees.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

