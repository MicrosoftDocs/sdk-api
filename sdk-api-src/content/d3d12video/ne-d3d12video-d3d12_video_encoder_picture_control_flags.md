---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS
ms.date: 06/30/2021
targetos: Windows
description: Specifies video encoder picture control flags.
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
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS
dev_langs:
 - c++
---

## -description

Specifies video encoder picture control flags.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_NONE

None.

### -field D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAG_USED_AS_REFERENCE_PICTURE

The associated frame will be used as a reference frame in future encode commands. Indicates that the reconstructed picture along with the bitstream should be output for the host to place it in future calls in the reconstructed pictures reference list. 

Note that there might be limitations for some frame types to be marked as references. Check feature support before setting this value.


## -remarks

Values from this enumeration are used by [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md).

If this flag is not set, the [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE.pReconstructedPicture](ns-d3d12video-d3d12_video_encoder_reconstructed_picture.md) can be nullptr in the associated call to [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md).

## -see-also

