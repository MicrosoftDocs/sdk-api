---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FORMAT_CAPS
title: D3D11_VIDEO_PROCESSOR_FORMAT_CAPS (d3d11.h)
description: Defines capabilities related to input formats for a Microsoft Direct3D 11 video processor.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_FORMAT_CAPS","D3D11_VIDEO_PROCESSOR_FORMAT_CAPS enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED","D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_INTERLACED","D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY","D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_PROCAMP","d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS","d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED","d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_INTERLACED","d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY","d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_PROCAMP","mf.d3d11_video_processor_format_caps"]
old-location: mf\d3d11_video_processor_format_caps.htm
tech.root: mf
ms.assetid: E14D25B7-9F97-465A-ADA5-820BB2952E00
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FORMAT_CAPS, D3D11_VIDEO_PROCESSOR_FORMAT_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED, D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_INTERLACED, D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY, D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_PROCAMP, d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED, d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_INTERLACED, d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY, d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_PROCAMP, mf.d3d11_video_processor_format_caps
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_FORMAT_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_FORMAT_CAPS
 - d3d11/D3D11_VIDEO_PROCESSOR_FORMAT_CAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_FORMAT_CAPS
---

# D3D11_VIDEO_PROCESSOR_FORMAT_CAPS enumeration


## -description

Defines capabilities related to input formats for a Microsoft Direct3D 11 video processor.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_INTERLACED:0x1

The video processor can deinterlace an input stream that contains interlaced RGB video.

### -field D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_PROCAMP:0x2

The video processor can perform color adjustment on RGB video.

### -field D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY:0x4

The video processor can perform luma keying on RGB video.

### -field D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED:0x8

The video processor can deinterlace input streams with palettized color formats.

## -remarks

These flags define video processing capabilities that usually are not needed, and that video devices are therefore not required to support.

The first three flags relate to RGB support for functions that are normally applied to YCbCr video: deinterlacing, color adjustment, and luma keying. A device that supports these functions for YCbCr is not required  to support them for RGB input. Supporting RGB input for these functions  is  an additional capability, reflected by these constants. Note that the driver might convert the input to another color space, perform the indicated function, and then convert the result back to RGB.
      

Similarly, a device that supports deinterlacing is not required to support deinterlacing of palettized formats. This capability is indicated by the <b>D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_PALETTE_INTERLACED</b> flag.

## -see-also

<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
