---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
ms.date: 06/29/2021
targetos: Windows
description: Represents the picture level control elements for the associated EncodeFrame command for multiple codecs.
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
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA
dev_langs:
 - c++
---

## -description

Represents the picture level control elements for the associated [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) command for multiple codecs.

## -struct-fields

### -field DataSize

The data size of the provided picture level control structure.

### -field pH264PicData

A pointer to a [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264.md) representing the picture level control elements for H.264 encoding.

### -field pHEVCPicData

A pointer to a [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC](ns-d3d12video-d3d12_video_encoder_reference_picture_descriptor_hevc.md) representing the picture level control elements for H.264 encoding.

## -remarks

Slice-level picture reference lists reordering is unsupported.

Weighted inter-prediction is unsupported.


## -see-also

