---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
title: D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
description: Specifies the alpha fill mode for video processing. (D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE)
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE","D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE",""]
tech.root: mf
ms.assetid: 828e0cbe-17ff-4830-8c95-997a6d53a994
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE, D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE,
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
req.typenames: D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
 - d3d12video/D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE
---

# D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE enumeration


## -description

Specifies the alpha fill mode for video processing. This value is used by the [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](ns-d3d12video-d3d12_video_process_output_stream_desc.md) structure.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_OPAQUE 

Alpha values inside the target rectangle are set to opaque.

### -field D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_BACKGROUND 

Alpha values inside the target rectangle are set to the alpha value specified in the background color.

### -field D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_DESTINATION 

Existing alpha values remain unchanged in the output surface.

### -field D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_SOURCE_STREAM 

Alpha values are taken from an input stream, scaled, and copied to the corresponding destination rectangle for that stream. The input stream is specified in the *AlphaFillModeSourceStreamIndex* member of <a href="ns-d3d12video-d3d12_video_process_input_stream_arguments.md">D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS</a>.

If the input stream does not have alpha data, the video processor sets the alpha values in the target rectangle to opaque. If the input stream is disabled or the source rectangle is empty, the alpha values in the target rectangle are not modified.

## -remarks

**D3D12_VIDEO_PROCESS_ALPHA_FILL_MODE_OPAQUE** must be always supported.  The background, destination, and source stream modes are only supported when the driver reports [D3D12_VIDEO_PROCESS_FEATURE_FLAG_ALPHA_FILL](ne-d3d12video-d3d12_video_process_feature_flags.md).

## -see-also

