---
UID: NE:d3d12video.D3D12_FEATURE_VIDEO
title: D3D12_FEATURE_VIDEO
description: Specifies a Direct3D 12 video feature or feature set to query about.
helpviewer_keywords: ["D3D12_FEATURE_VIDEO","D3D12_FEATURE_VIDEO",""]
tech.root: mf
ms.assetid: 19381358-07c5-4244-a28b-52b568da3b7c
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_VIDEO, D3D12_FEATURE_VIDEO,
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
req.typenames: D3D12_FEATURE_VIDEO
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_VIDEO
 - d3d12video/D3D12_FEATURE_VIDEO
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_VIDEO
---

# D3D12_FEATURE_VIDEO enumeration


## -description

Specifies a Direct3D 12 video feature or feature set to query about. When you want to query for the level to which an adapter supports a feature, pass one of these values to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md).

## -enum-fields

### -field D3D12_FEATURE_VIDEO_DECODE_SUPPORT 

Check if a decode profile, bitstream encryption, resolution, and format are supported.  The result is a <a href="ne-d3d12video-d3d12_video_decode_tier.md">D3D12_VIDEO_DECODE_TIER</a> indicating the level of support.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decode_support.md">D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT</a>.

### -field D3D12_FEATURE_VIDEO_DECODE_PROFILES 

Retrieve the list of decode profiles supported by the adapter.  Call **CheckFeatureSupport** specifying the feature D3D12_FEATURE_VIDEO_DECODE_PROFILE_COUNT to get the number of profiles before calling **CheckFeatureSupport** for the D3D12_FEATURE_VIDEO_DECODE_PROFILES feature.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decode_profiles.md">D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES</a>.

### -field D3D12_FEATURE_VIDEO_DECODE_FORMATS 

Retrieves the list of supported decode formats for a <a href="ns-d3d12video-d3d12_video_decode_configuration.md">D3D12_VIDEO_DECODE_CONFIGURATION</a>. Call **CheckFeatureSupport** specifying the feature D3D12_FEATURE_VIDEO_DECODE_FORMAT_COUNT to get the number of profiles before calling **CheckFeatureSupport** for the D3D12_FEATURE_VIDEO_DECODE_PROFILES feature.The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decode_formats.md">D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS</a>.

### -field D3D12_FEATURE_VIDEO_DECODE_CONVERSION_SUPPORT 

Check if a colorspace conversion, format conversion, and scale are supported.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decode_conversion_support.md">D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT</a>.

### -field D3D12_FEATURE_VIDEO_PROCESS_SUPPORT 

Retrieves the video processor capabilities.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_process_support.md">D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT</a>.

### -field D3D12_FEATURE_VIDEO_PROCESS_MAX_INPUT_STREAMS 

Retrieves the maximum number of streams that can be enabled at the same time.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_process_max_input_streams.md">D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS</a>.

### -field D3D12_FEATURE_VIDEO_PROCESS_REFERENCE_INFO 

Retrieves the number of past and future frames required for a given deinterlace mode, filters, frame rate conversion, and features.  The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_process_reference_info.md">D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO</a>.

### -field D3D12_FEATURE_VIDEO_DECODER_HEAP_SIZE 

Checks the allocation size of a video decoder heap. The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decoder_heap_size.md">D3D12_FEATURE_DATA_VIDEO_DECODER_HEAP_SIZE</a>. For information on residency budgeting for heaps, see [Residency](/windows/win32/direct3d12/residency).

### -field D3D12_FEATURE_VIDEO_PROCESSOR_SIZE 

Checks the allocation size of a video processor heap. The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_processor_size.md">D3D12_FEATURE_DATA_VIDEO_PROCESSOR_SIZE</a>. For information on residency budgeting for heaps, see [Residency](/windows/win32/direct3d12/residency).

### -field D3D12_FEATURE_VIDEO_DECODE_PROFILE_COUNT 

Retrieves the number of supported decoder profiles. The returned count is used when querying for **D3D12_FEATURE_VIDEO_DECODE_PROFILES**.

### -field D3D12_FEATURE_VIDEO_DECODE_FORMAT_COUNT 

Retrieves the number of supported decoder profiles. The returned count is used when querying for **D3D12_FEATURE_VIDEO_DECODE_FORMATS**.

### -field D3D12_FEATURE_VIDEO_ARCHITECTURE 

Indicates if the video engine is IO coherent with the CPU.

### -field D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM 

Retrieves the supported components, bin count, and counter bit depth for the a decode histogram with the specified decode profile, resolution, and format. The associated data structure is <a href="ns-d3d12video-d3d12_feature_data_video_decode_histogram.md">D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM</a>.

### -field D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR

Retrieves the supported resolutions, search block sizes, and precision for motion estimation. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](ns-d3d12video-d3d12_feature_data_video_motion_estimator.md).

### -field D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_SIZE

Checks the allocation size of a motion estimator heap. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](ns-d3d12video-d3d12_feature_data_video_motion_estimator_size.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_COUNT

Retrieves the supported number of video extension commands.  The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](ns-d3d12video-d3d12_feature_data_video_extension_command_count.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMANDS

Retrieves a list of [D3D12_VIDEO_EXTENSION_COMMAND_INFO](ns-d3d12video-d3d12_video_extension_command_info.md) structures describing video extension commands. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](ns-d3d12video-d3d12_feature_data_video_extension_command_count.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT

Retrieves the parameter count for the specified parameter stage. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS

Retrieves a list of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](ns-d3d12video-d3d12_video_extension_command_parameter_info.md) structures describing video extension command parameters for the specified parameter stage. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](ns-d3d12video-d3d12_feature_data_video_extension_command_parameters.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_SUPPORT

Queries for command-defined support information. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](ns-d3d12video-d3d12_feature_data_video_extension_command_support.md).

### -field D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_SIZE

Checks the allocation size of a video extension command. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](ns-d3d12video-d3d12_feature_data_video_extension_command_size.md).

### -field D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES

Checks support for motion estimation with protected resources. The associated data structure is [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources.md).

## -remarks

## -see-also

