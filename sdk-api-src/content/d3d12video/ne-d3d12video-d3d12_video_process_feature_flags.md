---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_FEATURE_FLAGS
title: D3D12_VIDEO_PROCESS_FEATURE_FLAGS
description: Specifies the features that a video processor can support.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_FEATURE_FLAGS","D3D12_VIDEO_PROCESS_FEATURE_FLAGS",""]
tech.root: mf
ms.assetid: 5471ef83-d960-45ee-9d74-8ef779a12f43
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_FEATURE_FLAGS, D3D12_VIDEO_PROCESS_FEATURE_FLAGS,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_PROCESS_FEATURE_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_FEATURE_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_FEATURE_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_FEATURE_FLAGS
---

# D3D12_VIDEO_PROCESS_FEATURE_FLAGS enumeration


## -description

Specifies the features that a video processor can support.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_NONE 

No features are supported.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_ALPHA_FILL 

The video processor can set alpha values on the output pixels. The alpha fill mode is used in <a href="ns-d3d12video-d3d12_video_process_output_stream_desc.md">D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC</a>.  <a href="ne-d3d12video-d3d12_video_process_alpha_fill_mode.md">D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_OPAQUE</a> must be always supported.  The background, destination, and source stream modes are only supported when the driver reports D3D12_VIDEO_PROCESS_FEATURE_FLAG_ALPHA_FILL.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_LUMA_KEY 

The video processor can perform luma keying.  Luma keying is configured via the **D3D12_VIDEO_PROCESS_LUMA_KEY** member of the <a href="ns-d3d12video-d3d12_video_process_input_stream_arguments.md">D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS</a> structure. For more information see <a href=ns-d3d12video-d3d12_video_process_luma_key"">D3D12_VIDEO_PROCESS_LUMA_KEY</a>.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_STEREO 

The video processor can support 3D stereo video. For more information, see <a href="ne-d3d12video-d3d12_video_frame_stereo_format.md">D3D12_VIDEO_FRAME_STEREO_FORMAT</a>.

All drivers setting this capability must support the following stereo formats: D3D12_VIDEO_PROCESS_STEREO_FORMAT_HORIZONTAL, D3D12_VIDEO_PROCESS_STEREO_FORMAT_VERTICAL, and D3D12_VIDEO_PROCESS_STEREO_FORMAT_SEPARATE.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_ROTATION 

The driver can rotate the input data either 90, 180, or 270 degrees clockwise as part of the video processing operation.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_FLIP 

The driver can flip the input data horizontally or vertically, together or separately with a video rotation operation.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_ALPHA_BLENDING 

Alpha blending and a planar alpha may be set in the **AlphaBlending** member of the <a href="ns-d3d12video-d3d12_video_process_input_stream_arguments.md">D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS</a> structure.  For more information see <a href="ns-d3d12video-d3d12_video_process_alpha_blending.md">D3D12_VIDEO_PROCESS_ALPHA_BLENDING</a>.

### -field D3D12_VIDEO_PROCESS_FEATURE_FLAG_PIXEL_ASPECT_RATIO 

The driver supports changing the pixel aspect ratio.  If the driver does not report this capability, then the **SourceAspectRatio** and **DestinationAspectRatio** members of <a href="ns-d3d12video-d3d12_video_process_input_stream_arguments.md">D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS</a> structure must indicate a 1:1 aspect ratio.

## -remarks

## -see-also

