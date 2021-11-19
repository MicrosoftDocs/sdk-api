---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE
ms.date: 06/07/2021
targetos: Windows
description: Specifies video encoder rate control modes.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE
dev_langs:
 - c++
---

## -description

Specifies video encoder rate control modes.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_ABSOLUTE_QP_MAP

No rate control budgeting. Each [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) call will interpret the the QP values in the **pRateControlQPMap** field of the [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264.md) or [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_hevc.md) structure as a map of absolute QP values.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_CQP

Constant quantization parameter rate control mode.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_CBR

Constant bit rate rate control mode.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_VBR

Variable bit rate control mode.

### -field D3D12_VIDEO_ENCODER_RATE_CONTROL_MODE_QVBR

Constant quality target rate variable rate control mode.

## -remarks

## -see-also

[EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md)

[D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_h264.md)

[D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data_hevc.md)


