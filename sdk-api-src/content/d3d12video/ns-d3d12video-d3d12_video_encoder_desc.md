---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_DESC
tech.root: mf
title: D3D12_VIDEO_ENCODER_DESC
ms.date: 06/21/2021
targetos: Windows
description: Describes an ID3D12VideoEncoder.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_DESC
f1_keywords:
 - D3D12_VIDEO_ENCODER_DESC
 - d3d12video/D3D12_VIDEO_ENCODER_DESC
dev_langs:
 - c++
---

## -description

Describes an [ID3D12VideoEncoder](nn-d3d12video-id3d12videoencoder.md). Pass this structure into [ID3D12VideoDevice3::CreateVideoEncoder](nf-d3d12video-id3d12videodevice3-createvideoencoder.md) to create an instance of **ID3D12VideoEncoder**.

## -struct-fields

### -field NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Flags

A bitwise OR combination of values from the [D3D12_VIDEO_ENCODER_FLAGS](ne-d3d12video-d3d12_video_encoder_flags.md) specifying the flags for encoder creation.

### -field EncodeCodec

A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the desired codec.

### -field EncodeProfile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) structure specifying the desired encoding profile.

### -field InputFormat

A [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) specifying the format of the source stream.

### -field CodecConfiguration

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_codec_configuration.md) structure specifying codec configuration parameters.

### -field MaxMotionEstimationPrecision

A value from the [D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE](ne-d3d12video-d3d12_video_encoder_motion_estimation_precision_mode.md) enumeration the maximum number of motion vectors allowed.

## -remarks

## -see-also

