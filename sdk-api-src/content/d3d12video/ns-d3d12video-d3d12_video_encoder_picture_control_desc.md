---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
ms.date: Describes a video encoder picture control.
targetos: Windows
description: 06/30/2021
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
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC
dev_langs:
 - c++
---

## -description

Describes a video encoder picture control.

## -struct-fields

### -field IntraRefreshFrameIndex



When requesting an intra-refresh wave for IntraRefreshFramesDuration frames by specifying the [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_FLAG_REQUEST_INTRA_REFRESH](ne-d3d12video-d3d12_video_encoder_sequence_control_flags.md) flag, this value indicates, for the current picture, the index of the frame in the intra-refresh wave. The value range is set by the host between 0 and [IntraRefreshFramesDuration](ns-d3d12video-d3d12_video_encoder_intra_refresh.md) to hint the status of the intra-refresh session to the driver.

### -field Flags

A bitwise OR combination of values from the [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_FLAGS](ne-d3d12video-d3d12_video_encoder_picture_control_flags.md) enumeration specifying the picture control descriptor flags.

### -field PictureControlCodecData

A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data.md) structure containing codec-specific picture control data. Depending of the selected rate control mode the QP values are interpreted differently. 

### -field ReferenceFrames

A [D3D12_VIDEO_ENCODE_REFERENCE_FRAMES](ns-d3d12video-d3d12_video_encode_reference_frames.md) structure containing the reconstructed pictures from the past encoding operations outputs.

## -remarks

The following remarks provide guidance for frame management.

The host calls [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) in encode order based in the picture type periodic sequence configured in the codec GOP structure after doing the B-frame reordering by POC if needed. Different codecs will use their own ways of indexing this structure and keeping their state metadata. Refer to the codec picture parameters also passed in the **EncodeFrame** operation that contain such details.

[D3D12_VIDEO_ENCODER_SUPPORT_FLAG_RECONSTRUCTED_FRAMES_REQUIRE_TEXTURE_ARRAYS](ne-d3d12video-d3d12_video_encoder_support_flags.md) specifies the requirement of texture arrays for the *ppTexture2Ds* and *pSubresources* fields of the **D3D12_VIDEO_ENCODE_REFERENCE_FRAMES** structure.

The output of the encode operation for a given frame must also return the reconstructed picture if marked as used as reference for future usage in next frames, the client passes the reconstructed pictures in future **EncodeFrame** commands.

If coding temporal layers, a picture can only use as references pictures on lower *TemporalLayerIndex* than its own. The temporal layer indices are specified in the picture control structure and in the reference picture descriptors. 

The HW limitations for the number of reference pictures are expressed in terms of the maximum number of elements present in L0 (MaxL0ReferencesForP/MaxL0ReferencesForB) and L1 (MaxL1ReferencesForB) lists and limiting by MaxDPBCapacity the maximum number of unique indices in (L0 union L1) that map into the value of *pReferenceFramesReconPictureDescriptors* provided in [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA](ns-d3d12video-d3d12_video_encoder_picture_control_codec_data.md).

There's no limitation to the number of DPB entries being passed in *pReferenceFramesReconPictureDescriptors*, but instead in the number of entries on that array being references by the L0 and L1 lists. This allows the user to track the state of a DPB in *pReferenceFramesReconPictureDescriptors* within the restrictions defined by the codec standard limitations and only use a subset restricted by the hardware limitations when calling **EncodeFrame**. For example, for HEVC encoding, the caller could keep track of the latest 15 encoded pictures in *pReferenceFramesReconPictureDescriptors* but only use a subset of the pictures that falls within the hardware restrictions, by assigning a limited number of unique indices in the L0 and L1 lists.

Note that a request for an IDR frame will act as a barrier between frame references and the DPB buffer and its state might need to be flushed accordingly by the host.


## -see-also

