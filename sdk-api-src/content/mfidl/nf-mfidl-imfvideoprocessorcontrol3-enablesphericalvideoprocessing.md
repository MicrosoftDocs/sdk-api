---
UID: NF:mfidl.IMFVideoProcessorControl3.EnableSphericalVideoProcessing
tech.root: mf
title: IMFVideoProcessorControl3::EnableSphericalVideoProcessing
ms.date: 09/09/2025
targetos: Windows
description: Enables spherical video rendering (360 video).
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
 - IMFVideoProcessorControl3::EnableSphericalVideoProcessing
f1_keywords:
 - IMFVideoProcessorControl3::EnableSphericalVideoProcessing
 - mfidl/IMFVideoProcessorControl3::EnableSphericalVideoProcessing
dev_langs:
 - c++
helpviewer_keywords:
 - EnableSphericalVideoProcessing
---

## -description

Enables spherical video rendering (360 video).

## -parameters

### -param fEnable [in]

A **BOOL** specifying Whether rendering is enabled.

### -param eFormat [in]

A member of the [MFVideoSphericalFormat](ne-mfidl-mfvideosphericalformat.md) enumeration specifying the type of spherical video to render.

### -param eProjectionMode [in]

A member of the [MFVideoSphericalProjectionMode](ne-mfidl-mfvideosphericalprojectionmode.md) enumeration specifying how the video should be projected.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.


## -remarks



## -see-also

