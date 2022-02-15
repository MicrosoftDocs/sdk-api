---
UID: NE:dxvahd._DXVAHD_DEVICE_CAPS
title: DXVAHD_DEVICE_CAPS (dxvahd.h)
description: Defines video processing capabilities for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_DEVICE_CAPS","DXVAHD_DEVICE_CAPS enumeration [Media Foundation]","DXVAHD_DEVICE_CAPS_LINEAR_SPACE","DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION","DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION","DXVAHD_DEVICE_CAPS_xvYCC","dxvahd/DXVAHD_DEVICE_CAPS","dxvahd/DXVAHD_DEVICE_CAPS_LINEAR_SPACE","dxvahd/DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION","dxvahd/DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION","dxvahd/DXVAHD_DEVICE_CAPS_xvYCC","mf.dxvahd_device_caps"]
old-location: mf\dxvahd_device_caps.htm
tech.root: mf
ms.assetid: 1f3dde4c-cd9d-4361-b2b2-db3c9d2ea146
ms.date: 12/05/2018
ms.keywords: DXVAHD_DEVICE_CAPS, DXVAHD_DEVICE_CAPS enumeration [Media Foundation], DXVAHD_DEVICE_CAPS_LINEAR_SPACE, DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION, DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, DXVAHD_DEVICE_CAPS_xvYCC, dxvahd/DXVAHD_DEVICE_CAPS, dxvahd/DXVAHD_DEVICE_CAPS_LINEAR_SPACE, dxvahd/DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION, dxvahd/DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, dxvahd/DXVAHD_DEVICE_CAPS_xvYCC, mf.dxvahd_device_caps
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_DEVICE_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_DEVICE_CAPS
 - dxvahd/_DXVAHD_DEVICE_CAPS
 - DXVAHD_DEVICE_CAPS
 - dxvahd/DXVAHD_DEVICE_CAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_DEVICE_CAPS
---

# DXVAHD_DEVICE_CAPS enumeration


## -description

Defines video processing capabilities for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -enum-fields

### -field DXVAHD_DEVICE_CAPS_LINEAR_SPACE:0x1

The device can blend video content in linear color space. Most video content is gamma corrected, resulting in nonlinear values. If the DXVA-HD device sets this flag, it means the device converts colors to linear space before blending, which produces better results.

### -field DXVAHD_DEVICE_CAPS_xvYCC:0x2

The device supports the xvYCC color space for YCbCr data.

### -field DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION:0x4

The device can perform range conversion when the input and output are both RGB but use different color ranges (0-255 or 16-235, for 8-bit RGB).

### -field DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION:0x8

The device can apply a matrix conversion to YCbCr values when the input and output are both YCbCr. For example, the driver can convert colors from BT.601 to BT.709.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
