---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS
ms.date: 04/07/2026
targetos: Windows
description: Specifies support flags for rate control frame analysis in video encoding.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAGS
dev_langs:
 - c++
---

## -description

Specifies support flags for rate control frame analysis in video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_NONE : 0x0

Indicates no support.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_INTRACODED_FRAME_SUPPORTED : 0x1

Indicates support for two pass frame analysis for intra coded frame types.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_UNIDIR_INTER_FRAME_SUPPORTED : 0x2

Indicates support for two pass frame analysis for inter coded unidirectional frame types.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_BIDIR_INTER_FRAME_SUPPORTED : 0x4

Indicates support for two pass frame analysis for inter coded bidirectional frame types. When [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RATE_CONTROL_FRAME_ANALYSIS_AVAILABLE](ne-d3d12video-d3d12_video_encoder_support_flags.md) is supported, this flag must also be supported when querying [D3D12_FEATURE_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS](ne-d3d12video-d3d12_feature_video.md) for *Pow2DownscaleFactor* equal to 0.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_EXTERNAL_DPB_DOWNSCALING : 0x8

Indicates support for the app to optionally skip the reconstructed picture output writing for the 1st pass and externally downscale the reconstructed picture texture to generate the lower resolution corresponding DPB textures. Using external downscaling may provide better quality at a higher performance cost, so apps can choose this as a trade-off.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_DYNAMIC_1ST_PASS_SKIP : 0x10

Indicates support for dynamically toggling [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_FRAME_ANALYSIS](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md) on an encode session associated with an [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md) with two pass enabled. Disabling that flag makes the driver skip the 1st (lower resolution) pass for the associated EncodeFrame1 command.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS_SUPPORT_FLAG_DYNAMIC_DOWNSCALE_FACTOR_CHANGE_KEY_FRAME : 0x20

Indicates support for changing the *Pow2DownscaleFactor* of the encode session associated [ID3D12VideoEncoderHeap1](nn-d3d12video-id3d12videoencoderheap1.md). Such change requires the app to re-create the **ID3D12VideoEncoderHeap1** object using the new *Pow2DownscaleFactor* parameter. This can only be done at KEY/IDR frames that clear the DPB.

## -remarks

The 1st pass corresponds to the lower resolution and the 2nd pass corresponds to the full resolution.

As the driver reports support for which individual frame types used in EncodeFrame1, the app can set [D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_FRAME_ANALYSIS](ne-d3d12video-d3d12_video_encoder_rate_control_flags.md). When the frame type is not supported by the driver, the app must not enable it.

Changing **D3D12_VIDEO_ENCODER_RATE_CONTROL_FLAG_ENABLE_FRAME_ANALYSIS** between frames must not trigger the app to set D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_RATE_CONTROL_CHANGE (or encoder recreation) if no other rate control change happened.

## -see-also

[D3D12_FEATURE_DATA_VIDEO_ENCODER_RATE_CONTROL_FRAME_ANALYSIS](ns-d3d12video-d3d12_feature_data_video_encoder_rate_control_frame_analysis.md)
