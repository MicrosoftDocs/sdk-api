---
UID: NS:mfapi._MFPinholeCameraIntrinsics
title: MFPinholeCameraIntrinsics (mfapi.h)
description: Contains zero or 1 pinhole camera intrinsic models that describe how to project a 3D point in physical world onto the 2D image frame of a camera.
helpviewer_keywords: ["MFPinholeCameraIntrinsics","MFPinholeCameraIntrinsics structure [Media Foundation]","PMFPinholeCameraIntrinsics","PMFPinholeCameraIntrinsics structure pointer [Media Foundation]","mf.mfpinholecameraintrinsics","mfapi/MFPinholeCameraIntrinsics","mfapi/PMFPinholeCameraIntrinsics"]
old-location: mf\mfpinholecameraintrinsics.htm
tech.root: mf
ms.assetid: 477F4DF6-CAE5-4BCD-A7D9-B1656DEA11E6
ms.date: 12/05/2018
ms.keywords: MFPinholeCameraIntrinsics, MFPinholeCameraIntrinsics structure [Media Foundation], PMFPinholeCameraIntrinsics, PMFPinholeCameraIntrinsics structure pointer [Media Foundation], mf.mfpinholecameraintrinsics, mfapi/MFPinholeCameraIntrinsics, mfapi/PMFPinholeCameraIntrinsics
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFPinholeCameraIntrinsics
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFPinholeCameraIntrinsics
 - mfapi/_MFPinholeCameraIntrinsics
 - MFPinholeCameraIntrinsics
 - mfapi/MFPinholeCameraIntrinsics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFPinholeCameraIntrinsics
---

# MFPinholeCameraIntrinsics structure


## -description

Contains zero or 1 pinhole camera intrinsic models that describe how to project a 3D point in physical world onto the 2D image frame of a camera. The conventions assumed by this structure imply a left-handed 3D coordinate system, with +X pointing to the right of the sensor, +Y pointing upwards from the sensor, and +Z pointing forward out of the sensor through the center (principal point) of the image.

## -struct-fields

### -field IntrinsicModelCount

The number of camera intrinsic models in the <i>IntrinsicModels</i> array.

### -field IntrinsicModels

The array of camera intrinsic models in the intrinsic data.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>