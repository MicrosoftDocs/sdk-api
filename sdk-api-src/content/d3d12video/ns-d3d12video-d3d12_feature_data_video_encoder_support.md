---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
ms.date: 06/13/2021
targetos: Windows
description: Retrieves values indicating support for the specified video encoding features and configuration values.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_SUPPORT](ne-d3d12video-d3d12_feature_video.md). Retrieves values indicating support for the specified video encoding features and configuration values.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which support is being queried.

### -field InputFormat

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) structure specifying the profile for which support is being queried.

### -field CodecConfiguration

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_codec_configuration.md) structure representing the codec configuration for which support is being queried.

### -field CodecGopSequence

A [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE](ns-d3d12video-d3d12_video_encoder_sequence_gop_structure.md) structure representing the GOP structure for which support is being queried.

### -field RateControl

A [D3D12_VIDEO_ENCODER_RATE_CONTROL](ns-d3d12video-d3d12_video_encoder_rate_control.md) representing the rate control settings for which support is being queried.

### -field IntraRefresh

A member of the [D3D12_VIDEO_ENCODER_INTRA_REFRESH_MODE](ne-d3d12video-d3d12_video_encoder_intra_refresh_mode.md) enumeration specifying the intra refresh mode for which support is being queried.

### -field SubregionFrameEncoding

A member of the [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md) enumeration, specifying the subregion layout mode for which support is being queried.

### -field ResolutionsListCount

A UINT specifying the number of resolutions provided in the *pResolutionList* field.

### -field pResolutionList

A pointer to an array of [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) specifying the picture resolutions for which support is being queried.

### -field MaxReferenceFramesInDPB

A UINT specifying Maximum number of previous reference frames to be used when calling [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) for inter-frames. This value is used to calculate the suggested level returned in the *SuggestedLevel* field.

### -field ValidationFlags

Receives a bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_VALIDATION_FLAGS](ne-d3d12video-d3d12_video_encoder_validation_flags.md) enumeration that provide additional details if the [D3D12_VIDEO_ENCODER_SUPPORT_FLAG_GENERAL_SUPPORT_OK](ne-d3d12video-d3d12_video_encoder_support_flags.md) flag is not set in the *SupportFlags* field. See **Remarks** for more information.

### -field SupportFlags

Receives a bitwise OR combination of flags from the [D3D12_VIDEO_ENCODER_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_support_flags.md) enumeration specifying support details for the specified encoder features and configuration values.

### -field SuggestedProfile

Receives a [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the recommended profile for the specified encoder features and configuration values.

### -field SuggestedLevel

Receives a [D3D12_VIDEO_ENCODER_LEVEL_SETTING](ns-d3d12video-d3d12_video_encoder_level_setting.md) specifying the recommended profile for the specified encoder features and configuration values. The recommended level assumes the maximum resolution from the list provided in *pResolutionList*.

### -field pResolutionDependentSupport

Receives a pointer to an array of [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) structures specifying resolution-dependent support limits corresponding to the resolutions provided in *pResolutionList*.

## -remarks

The support granted or rejected by this query indicates simultaneous support for all the features selected to be used in the same encoding session. There can be features that are supported individually when queried with individual query calls but not supported simultaneously.

For example, there can be support for intra refresh when checking [D3D12_FEATURE_VIDEO_ENCODER_INTRA_REFRESH_MODE](ne-d3d12video-d3d12_feature_video.md) and there can be support for B frames when checking [D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264.MaxL1ReferencesForB](ns-d3d12video-d3d12_video_encoder_codec_picture_control_support_h264.md) > 0. But it can be the case that intra refresh and B frames are not supported simultaneously. In this case, querying **D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT** with CodecGopSequence containing B frames and intra refresh row-based mode, the **D3D12_VIDEO_ENCODER_SUPPORT_FLAG_GENERAL_SUPPORT_OK** flag will be set off.


## -see-also

