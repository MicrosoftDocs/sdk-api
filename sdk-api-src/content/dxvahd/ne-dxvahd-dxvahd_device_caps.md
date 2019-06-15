---
UID: NE:dxvahd._DXVAHD_DEVICE_CAPS
title: DXVAHD_DEVICE_CAPS (dxvahd.h)
author: windows-sdk-content
description: Defines video processing capabilities for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_device_caps.htm
tech.root: medfound
ms.assetid: 1f3dde4c-cd9d-4361-b2b2-db3c9d2ea146
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXVAHD_DEVICE_CAPS, DXVAHD_DEVICE_CAPS enumeration [Media Foundation], DXVAHD_DEVICE_CAPS_LINEAR_SPACE, DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION, DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, DXVAHD_DEVICE_CAPS_xvYCC, dxvahd/DXVAHD_DEVICE_CAPS, dxvahd/DXVAHD_DEVICE_CAPS_LINEAR_SPACE, dxvahd/DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION, dxvahd/DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, dxvahd/DXVAHD_DEVICE_CAPS_xvYCC, mf.dxvahd_device_caps
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_DEVICE_CAPS
product: Windows
targetos: Windows
req.typenames: DXVAHD_DEVICE_CAPS
req.redist: 
ms.custom: 19H1
---

# DXVAHD_DEVICE_CAPS enumeration


## -description


Defines video processing capabilities for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -enum-fields




### -field DXVAHD_DEVICE_CAPS_LINEAR_SPACE

The device can blend video content in linear color space. Most video content is gamma corrected, resulting in nonlinear values. If the DXVA-HD device sets this flag, it means the device converts colors to linear space before blending, which produces better results.



### -field DXVAHD_DEVICE_CAPS_xvYCC

The device supports the xvYCC color space for YCbCr data.


### -field DXVAHD_DEVICE_CAPS_RGB_RANGE_CONVERSION

The device can perform range conversion when the input and output are both RGB but use different color ranges (0-255 or 16-235, for 8-bit RGB).


### -field DXVAHD_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION

The device can apply a matrix conversion to YCbCr values when the input and output are both YCbCr. For example, the driver can convert colors from BT.601 to BT.709.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

