---
UID: NS:d3d11.D3D11_VIDEO_COLOR
title: D3D11_VIDEO_COLOR (d3d11.h)
description: Defines a color value for Microsoft Direct3D 11 video.
helpviewer_keywords: ["D3D11_VIDEO_COLOR","D3D11_VIDEO_COLOR structure [Media Foundation]","d3d11/D3D11_VIDEO_COLOR","mf.d3d11_video_color"]
old-location: mf\d3d11_video_color.htm
tech.root: mf
ms.assetid: F8E070EE-F8F6-4AAF-9A8A-6D0AF6B857B5
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_COLOR, D3D11_VIDEO_COLOR structure [Media Foundation], d3d11/D3D11_VIDEO_COLOR, mf.d3d11_video_color
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
req.typenames: D3D11_VIDEO_COLOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_COLOR
 - d3d11/D3D11_VIDEO_COLOR
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
 - D3D11_VIDEO_COLOR
---

# D3D11_VIDEO_COLOR structure


## -description

Defines a color value for Microsoft Direct3D 11 video.

## -struct-fields

### -field YCbCr

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_color_ycbcra">D3D11_VIDEO_COLOR_YCbCrA</a> structure that contains a YCbCr color value.

### -field RGBA

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_color_rgba">D3D11_VIDEO_COLOR_RGBA</a> structure that contains an RGB color value.

## -remarks

The anonymous union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.

## -see-also

<a href="/windows/desktop/medfound/about-yuv-video">About YUV Video</a>



<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>