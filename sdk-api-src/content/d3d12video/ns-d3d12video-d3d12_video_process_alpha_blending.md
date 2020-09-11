---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_ALPHA_BLENDING
title: D3D12_VIDEO_PROCESS_ALPHA_BLENDING
description: Specifies alpha blending parameters for video processing.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_ALPHA_BLENDING","D3D12_VIDEO_PROCESS_ALPHA_BLENDING",""]
tech.root: mf
ms.assetid: 8907413b-b313-4b9e-bbe7-7e6c2a58de68
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_ALPHA_BLENDING, D3D12_VIDEO_PROCESS_ALPHA_BLENDING,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_PROCESS_ALPHA_BLENDING
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_ALPHA_BLENDING
 - d3d12video/D3D12_VIDEO_PROCESS_ALPHA_BLENDING
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_ALPHA_BLENDING
---

# D3D12_VIDEO_PROCESS_ALPHA_BLENDING structure


## -description

Specifies alpha blending parameters for video processing. Used by the [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS]ns-d3d12video-d3d12_video_process_input_stream_arguments) structure.

## -struct-fields

### -field Enable

A boolean value specifying whether alpha blending is enabled.

### -field Alpha

 
The planar alpha value. The value can range from 0.0 (transparent) to 1.0 (opaque). If *Enable* is FALSe, this parameter is ignored.

## -remarks

For each pixel, the destination color value is computed as follows:

`Cd = Cs * (As * Ap * Ae) + Cd * (1.0 - As * Ap * Ae)`

where:

- Cd = The color value of the destination pixel
- Cs = The color value of the source pixel
- As = The per-pixel source alpha
- Ap = The planar alpha value
- Ae = The palette-entry alpha value, or 1.0 (palette-entry alpha values apply only to palettized color formats)

## -see-also

