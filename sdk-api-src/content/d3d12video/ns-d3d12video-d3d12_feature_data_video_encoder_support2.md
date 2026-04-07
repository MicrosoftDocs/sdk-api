---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
ms.date: 04/07/2026
targetos: Windows
description: Provides data for checking extended video encoder support including QPMap, dirty regions, and motion search.
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
req.target-min-winverclnt:
req.target-min-winversvr:
req.target-type:
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
req.umdf-ver:
req.unicode-ansi:
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT2
---

## -description

Extends D3D12_FEATURE_DATA_VIDEO_ENCODER_SUPPORT1 for the driver to report support details when enabling QPMap, dirty regions, and/or motion search hints features. If the driver does not support a given combination, it must report D3D12_VIDEO_ENCODER_SUPPORT_FLAG_NONE and specify conflicting features in [D3D12_VIDEO_ENCODER_VALIDATION_FLAGS](ne-d3d12video-d3d12_video_encoder_validation_flags.md).

## -struct-fields

### -field NodeIndex

Input parameter. In multi-adapter operation, indicates which physical adapter of the device this operation applies to.

### -field Codec

Input parameter. A [D3D12_VIDEO_ENCODER_CODEC](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_video_encoder_codec) value specifying the codec.

### -field InputFormat

Input parameter. A DXGI_FORMAT value specifying the input format.

### -field CodecConfiguration

Input parameter. A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_codec_configuration) specifying the codec configuration.

### -field CodecGopSequence

Input parameter. A [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_sequence_gop_structure) specifying the GOP structure.

### -field RateControl

Input parameter. A [D3D12_VIDEO_ENCODER_RATE_CONTROL](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_rate_control) specifying the rate control.

### -field IntraRefresh

Input parameter. A [D3D12_VIDEO_ENCODER_INTRA_REFRESH_MODE](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_video_encoder_intra_refresh_mode) specifying the intra refresh mode.

### -field SubregionFrameEncoding

Input parameter. A [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_LAYOUT_MODE](ne-d3d12video-d3d12_video_encoder_frame_subregion_layout_mode.md) value specifying the subregion layout mode.

### -field ResolutionsListCount

Input parameter. The number of resolutions in pResolutionList.

### -field pResolutionList

Input parameter. Pointer to an array of [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_resolution_desc) structures specifying the resolutions.

### -field MaxReferenceFramesInDPB

Input parameter. The maximum number of reference frames in the decoded picture buffer.

### -field ValidationFlags

Output parameter. A combination of [D3D12_VIDEO_ENCODER_VALIDATION_FLAGS](ne-d3d12video-d3d12_video_encoder_validation_flags.md) indicating unsupported features.

### -field SupportFlags

Output parameter. A combination of [D3D12_VIDEO_ENCODER_SUPPORT_FLAGS](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_video_encoder_support_flags) indicating support.

### -field SuggestedProfile

Output parameter. A [D3D12_VIDEO_ENCODER_PROFILE_DESC](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_profile_desc) with the suggested profile.

### -field SuggestedLevel

Output parameter. A [D3D12_VIDEO_ENCODER_LEVEL_SETTING](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_level_setting) with the suggested level.

### -field pResolutionDependentSupport

Output parameter. Pointer to a caller-allocated array of [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS1](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits1.md) structures the driver fills for each resolution in pResolutionList.

### -field SubregionFrameEncodingData

A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_SUBREGIONS_LAYOUT_DATA](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_encoder_picture_control_subregions_layout_data) specifying the subregion layout data.

### -field MaxQualityVsSpeed

Output parameter. Maximum quality versus speed value.

### -field QPMap

Input parameter. A [D3D12_VIDEO_ENCODER_QPMAP_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_qpmap_configuration.md) specifying the intended QPMap configuration.

### -field DirtyRegions

Input parameter. A [D3D12_VIDEO_ENCODER_DIRTY_REGIONS_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_dirty_regions_configuration.md) specifying the intended dirty regions configuration.

### -field MotionSearch

Input parameter. A [D3D12_VIDEO_ENCODER_MOTION_SEARCH_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_motion_search_configuration.md) specifying the intended motion search configuration.

## -remarks

## -see-also
