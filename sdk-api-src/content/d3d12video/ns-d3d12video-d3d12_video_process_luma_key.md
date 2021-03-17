---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_LUMA_KEY
title: D3D12_VIDEO_PROCESS_LUMA_KEY
description: Specifies the settings used for luma keying.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_LUMA_KEY","D3D12_VIDEO_PROCESS_LUMA_KEY",""]
tech.root: mf
ms.assetid: c5183fec-5f5d-4a26-a35c-5ea60e7e1fe0
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_LUMA_KEY, D3D12_VIDEO_PROCESS_LUMA_KEY,
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
req.typenames: D3D12_VIDEO_PROCESS_LUMA_KEY
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_LUMA_KEY
 - d3d12video/D3D12_VIDEO_PROCESS_LUMA_KEY
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_LUMA_KEY
---

# D3D12_VIDEO_PROCESS_LUMA_KEY structure


## -description

Specifies the settings used for luma keying. This value is used with the [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](ns-d3d12video-d3d12_video_process_input_stream_desc.md) structure.

## -struct-fields

### -field Enable

 
A boolean value specifying whether luma keying is enabled.

### -field Lower

The lower bound for the luma key. The valid range is [0…1]. If *Enable* is FALSE, this parameter is ignored.

### -field Upper

 
The upper bound for the luma key. The valid range is [0…1]. If *Enable* is FALSE, this parameter is ignored.

## -remarks

The values of *Lower* and *Upper* give the lower and upper bounds of the luma key, using a nominal range of [0...1]. Given a format with n bits per channel, these values are converted to luma values as follows:

`val = f * ((1 << n)-1)`

Any pixel whose luma value falls within the upper and lower bounds (inclusive) is treated as transparent.  For example, if the pixel format uses 8-bit luma, the upper bound is calculated as follows:

`BYTE Y = BYTE(max(min(1.0, Upper), 0.0) * 255.0)`

Note that the value is clamped to the range [0...1] before multiplying by 255.

## -see-also

