---
UID: NE:dxvahd._DXVAHD_INPUT_FORMAT_CAPS
title: "_DXVAHD_INPUT_FORMAT_CAPS"
author: windows-driver-content
description: Defines capabilities related to input formats for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_input_format_caps.htm
old-project: medfound
ms.assetid: ddfff29c-3a40-4238-93e7-821c4ffc27af
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DXVAHD_INPUT_FORMAT_CAPS, DXVAHD_INPUT_FORMAT_CAPS enumeration [Media Foundation], DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED, DXVAHD_INPUT_FORMAT_CAPS_RGB_INTERLACED, DXVAHD_INPUT_FORMAT_CAPS_RGB_LUMA_KEY, DXVAHD_INPUT_FORMAT_CAPS_RGB_PROCAMP, _DXVAHD_INPUT_FORMAT_CAPS, dxvahd/DXVAHD_INPUT_FORMAT_CAPS, dxvahd/DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED, dxvahd/DXVAHD_INPUT_FORMAT_CAPS_RGB_INTERLACED, dxvahd/DXVAHD_INPUT_FORMAT_CAPS_RGB_LUMA_KEY, dxvahd/DXVAHD_INPUT_FORMAT_CAPS_RGB_PROCAMP, mf.dxvahd_input_format_caps
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DXVAHD_INPUT_FORMAT_CAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_INPUT_FORMAT_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_INPUT_FORMAT_CAPS enumeration


## -description


Defines capabilities related to input formats for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -enum-fields




### -field DXVAHD_INPUT_FORMAT_CAPS_RGB_INTERLACED

The device can deinterlace an input stream that contains interlaced RGB video.


### -field DXVAHD_INPUT_FORMAT_CAPS_RGB_PROCAMP

The device can perform color adjustment on RGB video.


### -field DXVAHD_INPUT_FORMAT_CAPS_RGB_LUMA_KEY

The device can perform luma keying on RGB video.


### -field DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED

The device can deinterlace input streams with palettized color formats.


## -remarks



These flags define video processing capabilities that are usually not needed, and therefore are not required for DXVA-HD devices to support.

The first three flags relate to RGB support for functions that are normally applied to YCbCr video: deinterlacing, color adjustment, and luma keying. A DXVA-HD device that supports these functions for YCbCr is not required  to support them for RGB input. Supporting RGB input for these functions  is  an additional capability, reflected by these constants. The driver might convert the input to another color space, perform the indicated function, and then convert the result back to RGB.

Similarly, a device that supports de-interlacing is not required to support deinterlacing of palettized formats. This capability is indicated by the <b>DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED</b> flag.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

