---
UID: NS:d3d11.D3D11_VIDEO_COLOR_YCbCrA
title: D3D11_VIDEO_COLOR_YCbCrA (d3d11.h)
description: Specifies a YCbCr color value. (D3D11_VIDEO_COLOR_YCbCrA)
helpviewer_keywords: ["D3D11_VIDEO_COLOR_YCbCrA","D3D11_VIDEO_COLOR_YCbCrA structure [Media Foundation]","d3d11/D3D11_VIDEO_COLOR_YCbCrA","mf.d3d11_video_color_ycbcra"]
old-location: mf\d3d11_video_color_ycbcra.htm
tech.root: mf
ms.assetid: 242D6032-62E5-4915-B074-6E595A12F912
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_COLOR_YCbCrA, D3D11_VIDEO_COLOR_YCbCrA structure [Media Foundation], d3d11/D3D11_VIDEO_COLOR_YCbCrA, mf.d3d11_video_color_ycbcra
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
req.typenames: D3D11_VIDEO_COLOR_YCbCrA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_COLOR_YCbCrA
 - d3d11/D3D11_VIDEO_COLOR_YCbCrA
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
 - D3D11_VIDEO_COLOR_YCbCrA
---

# D3D11_VIDEO_COLOR_YCbCrA structure


## -description

Specifies a YCbCr color value.

## -struct-fields

### -field Y

The Y luma value.

### -field Cb

The Cb chroma value.

### -field Cr

The Cr chroma value.

### -field A

The alpha value. Values range from 0 (transparent) to 1 (opaque).

## -remarks

Values have a nominal range of [0...1]. Given a format with  <i>n</i> bits per channel, the value of each color component is calculated as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

For example, for 8-bit YUV formats, <code>val = BYTE(f * 255.0)</code>.  Reference black is (0.0625, 0.5, 0.5), which corresponds to (16, 128, 128) in an 8-bit representation.

## -see-also

<a href="/windows/desktop/medfound/about-yuv-video">About YUV Video</a>



<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>
