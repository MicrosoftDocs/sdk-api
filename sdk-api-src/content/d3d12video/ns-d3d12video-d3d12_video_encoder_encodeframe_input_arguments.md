---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
ms.date: 07/01/2021
targetos: Windows
description: Represents input arguments to ID3D12VideoEncodeCommandList2::EncodeFrame.
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
req.typenames: D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS
dev_langs:
 - c++
---

## -description

Represents input arguments to [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md).

## -struct-fields

### -field SequenceControlDesc

A [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md) specifying the configuration for the video sequence

### -field PictureControlDesc

A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md) specifying the configuration for the video picture.

### -field pInputFrame

An [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource) representing the frame to encode.

### -field InputFrameSubresource

A UINT64 specifying the subresource index for *pInputFrame*.

### -field CurrentFrameBitstreamMetadataSize

A UINT64 specifying the number of bytes added to the final bitstream between the end of the last **EncodeFrame** compressed bitstream output and the current call output. This is intended to capture the size of any headers or metadata messages added by the client to the final bitstream which are used as a hint by the rate control algorithms to keep track of the full bitstream size.

## -remarks

## -see-also

