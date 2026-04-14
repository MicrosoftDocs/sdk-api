---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
ms.date: 04/07/2026
targetos: Windows
description: Describes the downscaled input frame and reference frames for two pass frame analysis.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
req.umdf-ver: 
req.unicode-ansi: 
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_ANALYSIS
dev_langs:
 - c++
---

## -description

Describes the downscaled input frame and reference frames for two pass frame analysis in a video encode operation.

## -struct-fields

### -field pDownscaledFrame

Pointer to an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) containing the downscaled input texture to perform two pass frame analysis. The downscaling factor is indicated by [D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md).*Pow2DownscaleFactor*. When the 1st pass is skipped, *pDownscaledFrame* is not necessary and NULL can be passed.

### -field Subresource

Subresource index for *pDownscaledFrame*.

### -field DownscaledReferences

A D3D12_VIDEO_ENCODE_REFERENCE_FRAMES containing the downscaled reference frame textures to perform two pass frame analysis. The downscaling factor is indicated by [D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md).*Pow2DownscaleFactor*.

## -remarks

The DPB snapshot and reference lists must be always mirrored for the parallel streams (full and downscaled resolution passes). *DownscaledReferences* and the corresponding full resolution reference frames must always have entries mirroring the same frames in the DPB, just in different resolutions.

## -see-also

[D3D12_VIDEO_ENCODER_HEAP_DESC1](ns-d3d12video-d3d12_video_encoder_heap_desc1.md)
