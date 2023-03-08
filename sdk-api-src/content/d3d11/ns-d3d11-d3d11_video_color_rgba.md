---
UID: NS:d3d11.D3D11_VIDEO_COLOR_RGBA
title: D3D11_VIDEO_COLOR_RGBA (d3d11.h)
description: Specifies an RGB color value. (D3D11_VIDEO_COLOR_RGBA)
helpviewer_keywords: ["D3D11_VIDEO_COLOR_RGBA","D3D11_VIDEO_COLOR_RGBA structure [Media Foundation]","d3d11/D3D11_VIDEO_COLOR_RGBA","mf.d3d11_video_color_rgba"]
old-location: mf\d3d11_video_color_rgba.htm
tech.root: mf
ms.assetid: DDD587DC-BB17-407D-9E9E-47015950A504
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_COLOR_RGBA, D3D11_VIDEO_COLOR_RGBA structure [Media Foundation], d3d11/D3D11_VIDEO_COLOR_RGBA, mf.d3d11_video_color_rgba
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
req.typenames: D3D11_VIDEO_COLOR_RGBA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_COLOR_RGBA
 - d3d11/D3D11_VIDEO_COLOR_RGBA
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
 - D3D11_VIDEO_COLOR_RGBA
---

# D3D11_VIDEO_COLOR_RGBA structure


## -description

Specifies an RGB color value.

## -struct-fields

### -field R

The red value.

### -field G

The green value.

### -field B

The blue value.

### -field A

The alpha value. Values range from 0 (transparent) to 1 (opaque).

## -remarks

The RGB values have a nominal range of [0...1]. For an RGB format with  <i>n</i> bits per channel, the value of each color component is calculated as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

For example, for RGB-32 (8 bits per channel), <code>val = BYTE(f * 255.0)</code>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>
