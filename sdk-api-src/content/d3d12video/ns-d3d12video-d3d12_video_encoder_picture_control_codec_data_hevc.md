---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
ms.date: 01/23/2025
targetos: Windows
description: Represents the picture level control elements for the associated EncodeFrame command for HEVC encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC
dev_langs:
 - c++
---

## -description

Represents the picture level control elements for the associated [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) command for HEVC encoding.

## -struct-fields

### -field Flags

A bitwise OR combination of values from the [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC_FLAGS](ne-d3d12video-d3d12_video_encoder_picture_control_codec_data_hevc_flags.md) enumeration specifying configuration flags for the frame being encoded.

### -field FrameType

A value from the [D3D12_VIDEO_ENCODER_FRAME_TYPE_HEVC](ne-d3d12video-d3d12_video_encoder_frame_type_hevc.md) enumeration specifying the picture type. Make sure that the codec-specific flags support the specified type. This selection must be kept in sync with the GOP structure configuration set by the host. Note that the GOP is defined in display order and this pic type selection must follow the GOP, but in encode order.

### -field slice_pic_parameter_set_id

A **UINT** specifying the value to be used in the slice headers of the current frame to reference the PPS.

### -field PictureOrderCountNumber

A **UINT** specifying the current frame display order.

### -field TemporalLayerIndex

A **UINT** specifying the picture layer number in temporal hierarchy. Check for the maximum number of layers in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC](ns-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc.md).

### -field List0ReferenceFramesCount

A **UINT** specifying the number of past frame references to be used for this frame. This value should be coherent with what was exposed in **D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC**.

### -field pList0ReferenceFrames

A pointer to a **UINT** array specifying the list of past frame reference frames to be used for this frame. Each integer value in this array indices into *pReferenceFramesReconPictureDescriptors* to reference pictures kept in the DPB.

### -field List1ReferenceFramesCount

A **UINT** specifying the number of future frame references to be used for this frame. This value should be coherent with what was exposed in **D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_HEVC**.

### -field pList1ReferenceFrames

A pointer to a **UINT** array specifying the list of future frame reference frames to be used for this frame. Each integer value in this array indices into *pReferenceFramesReconPictureDescriptors* to reference pictures kept in the DPB.

### -field ReferenceFramesReconPictureDescriptorsCount

A **UINT** specifying the number of entries in *pReferenceFramesReconPictureDescriptors*.

### -field pReferenceFramesReconPictureDescriptors

A pointer to a **UINT** array that describes the current state of the DPB buffer kept in [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC.ReferenceFrames](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md). The *pList0ReferenceFrames* and *pList1ReferenceFrames* lists indices map from past/future references into this descriptors array.

This array of descriptors, in turn, maps a reference picture for this frame into a resource index in the reconstructed pictures array **D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC.ReferenceFrames**. Additionally, for each reference picture it indicates the encode and display order number and whether it is a long term reference.

The size of this array always matches **D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC.ReferenceFrames.NumTextures** for the associated **EncodeFrame** command.


### -field List0RefPicModificationsCount

A **UINT** specifying the number of items in *pList0RefPicModifications*.

### -field pList0RefPicModifications

A pointer to a **UINT** array containing modification commands for the L0 list.

### -field List1RefPicModificationsCount

A **UINT** specifying the number of items in *pList1RefPicModifications*.

### -field pList1RefPicModifications

A pointer to a **UINT** array containing modification commands for the L1 list.

### -field QPMapValuesCount

A **UINT** specifying the number of elements present in *pRateControlQPMap*. This should match the number of coding blocks in the frame, rounding up the frame resolution to the closest aligned values.

### -field pRateControlQPMap

A pointer to an array of **Int8** containing, in row/column scan order, the QP map values to use on each squared region for this frame. The QP map dimensions can be calculated using the current resolution and [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.QPMapRegionPixelsSize](ns-d3d12video-d3d12_feature_data_video_encoder_resolution_support_limits.md) conveying the squared region sizes.

## -remarks


The following tables list the expected VPS, SPS and PPS Values for HEVC encoding.

### Level_idc mappings for HEVC


| D3D12 Level | Expected general_level_idc | Notes |
|--------|------------|------------|
D3D12_VIDEO_ENCODER_LEVELS_HEVC_1 | 30 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_2 | 60 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_21 | 63 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_3 | 90 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_31 | 93 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_4 | 120 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_41 | 123 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_5 | 150 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_51 | 153 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_52 | 156 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_6 | 180 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_61 | 183 | None |
D3D12_VIDEO_ENCODER_LEVELS_HEVC_62 | 186 | None |

### HEVC Video Parameter Set expected values

| Syntax element | Expected default value | Notes |
|--------|------------|------------|
vps_video_parameter_set_id | User specific | None |
vps_base_layer_internal_flag | 0 | None |
vps_base_layer_available_flag | 0 | None |
vps_max_layers_minus1 | 0 | None |
vps_max_sub_layers_minus1 | 0 | None |
vps_temporal_id_nesting_flag | 1 | None |
vps_reserved_ffff_16bits | 0xFFFF | None |
general_profile_space | 0 | None |
general_tier_flag | 1 for High tier, 0 for Main tier | None |
general_profile_idc | D3D12_VIDEO_ENCODER_PROFILE_HEVC enum value + 1 | None |
general_profile_compatibility_flag[general_profile_space] | 1 | None |
general_progressive_source_flag |1 | None |
general_interlaced_source_flag | 0 | None |
general_non_packed_constraint_flag | 1 | None |
general_frame_only_constraint_flag | 1 | None |
general_reserved_zero_44bits | 44 bit zeroes | None |
general_level_idc | Please see table above | None |
vps_sub_layer_ordering_info_present_flag | 0 | None |
vps_max_dec_pic_buffering_minus1[0] | (MaxReferenceFramesInDPB/*previous reference frames*/ + 1 /*additional current frame recon pic*/) - 1/**minus1 for header*/; | None |
vps_max_num_reorder_pics[0] | 0 if no B frames. vps_max_dec_pic_buffering_minus1 otherwise. | None |
vps_max_latency_increase_plus1[0] | 1 | None |
vps_max_layer_id | 0 | None |
vps_num_layer_sets_minus1 | 0 | None |
vps_timing_info_present_flag | 0 | None |
vps_extension_flag | 0 | None |

---

### HEVC Sequence Parameter Set expected values

| Syntax element | Expected default value | Notes |
|--------|------------|------------|
sps_video_parameter_set_id | User specific | None |
sps_max_sub_layers_minus1 | Same as in associated VPS | None |
sps_temporal_id_nesting_flag | Same as in associated VPS | None |
general_profile_space | 0 | None |
general_tier_flag | 1 for High tier, 0 for Main tier | None |
general_profile_idc | D3D12_VIDEO_ENCODER_PROFILE_HEVC enum value + 1 | None |
general_profile_compatibility_flag[general_profile_space] | 1 | None |
general_progressive_source_flag |1 | None |
general_interlaced_source_flag | 0 | None |
general_non_packed_constraint_flag | 1 | None |
general_frame_only_constraint_flag | 1 | None |
general_reserved_zero_44bits | 44 bit zeroes | None |
general_level_idc | Please see table above | None |
chroma_format_idc | 1 | 4.2.0 for NV12 and P010 |
pic_width_in_luma_samples | std::ceil(sequenceTargetResolution.Width / SubregionBlockPixelsSize)) * SubregionBlockPixelsSize | Use current frame resolution for D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.SubregionBlockPixelsSize  |
pic_height_in_luma_samples | std::ceil(sequenceTargetResolution.Height / SubregionBlockPixelsSize)) * SubregionBlockPixelsSize | Use current frame resolution for D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOLUTION_SUPPORT_LIMITS.SubregionBlockPixelsSize |
conformance_window_flag | 0 if resolution is aligned to SubregionBlockPixelsSize, 1 otherwise | None |
conf_win_left_offset | 0 | Only if conformance_windows_flag = 1 | 
conf_win_right_offset | (sps.pic_width_in_luma_samples - encodeResolution.Width) >> 1 | Only if conformance_windows_flag = 1 | 
conf_win_top_offset | 0 | Only if conformance_windows_flag = 1 | 
conf_win_bottom_offset | (sps.pic_height_in_luma_samples - encodeResolution.Height) >> 1 | Only if conformance_windows_flag = 1 | 
bit_depth_luma_minus8 | 0 for NV12, 2 for P010 | None |
bit_depth_luma_minus8 | 0 for NV12, 2 for P010 | None |
log2_max_pic_order_cnt_lsb_minus4 | Based on D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_HEVC | None |
sps_sub_layer_ordering_info_present_flag | Same as in associated VPS | None |
sps_max_dec_pic_buffering_minus1 | Same as in associated VPS | None |
sps_max_num_reorder_pics | Same as in associated VPS | None |
sps_max_latency_increase_plus1 | Same as in associated VPS | None |
log2_min_luma_coding_block_size_minus3 | std::log2(minCuSize) - 3) | For example MinCUSize=8 for D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_8x8 |
log2_diff_max_min_luma_coding_block_size | std::log2(maxCuSize) - std::log2(minCuSize)) | For example MaxCUSize=16 for D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_CUSIZE_16x16 |
log2_min_transform_block_size_minus2 | std::log2(minTuSize) - 2) |  For example MinTuSize=4 for D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_4x4 | |
log2_diff_max_min_transform_block_size | std::log2(maxTuSize) - std::log2(minTuSize)) | For example MaxTuSize=16 for D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_TUSIZE_16x16 | |
max_transform_hierarchy_depth_inter | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC | None |
max_transform_hierarchy_depth_inter | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC | None |
scaling_list_enabled_flag | 0 | None |
amp_enabled_flag | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_USE_ASYMETRIC_MOTION_PARTITION | None |
sample_adaptive_offset_enabled_flag | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_SAO_FILTER | None |
pcm_enabled_flag | 0 | None |
num_short_term_ref_pic_sets | 0 | None |
long_term_ref_pics_present_flag | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_LONG_TERM_REFERENCES | None |
num_long_term_ref_pics_sps | 0 | None |
sps_temporal_mvp_enabled_flag | 0 | None |
strong_intra_smoothing_enabled_flag | 0 | None |
vui_parameters_present_flag | 0 | None |
sps_extension_flag | 0 | None |

### HEVC Picture Parameter Set expected values

| Syntax element | Expected default value | Notes |
|--------|------------|------------|
pps_pic_parameter_set_id | User specific | None |
pps_seq_parameter_set_id | User specific | None |
dependent_slice_segments_enabled_flag | 0 | None |
output_flag_present_flag | 0 | None |
num_extra_slice_header_bits | 0 | None |
sign_data_hiding_enabled_flag | 0 | None |
cabac_init_present_flag | 1 | None |
num_ref_idx_lx_default_active_minus1[0] | std::max(static_cast&lt;INT&gt;(pictureControl.List0ReferenceFramesCount) - 1, 0)) | None |
num_ref_idx_lx_default_active_minus1[1] | std::max(static_cast&lt;INT&gt;(pictureControl.List1ReferenceFramesCount) - 1, 0)) | None |
init_qp_minus26 | 0 | None |
constrained_intra_pred_flag | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_USE_CONSTRAINED_INTRAPREDICTION | None |
transform_skip_enabled_flag | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_ENABLE_TRANSFORM_SKIPPING | None |
cu_qp_delta_enabled_flag | 1 | None |
diff_cu_qp_delta_depth | 0 | None |
pps_cb_qp_offset | 0 | None |
pps_cr_qp_offset | 0 | None |
pps_slice_chroma_qp_offsets_present_flag | 1 | None |
weighted_pred_flag | 0 | No support for weighted prediction in the API |
weighted_bipred_flag | 0 | No support for weighted prediction in the API |
transquant_bypass_enabled_flag | 0 | None |
tiles_enabled_flag | 0 | None |
entropy_coding_sync_enabled_flag | 0 | None |
pps_loop_filter_across_slices_enabled_flag  | Based on D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_FLAG_DISABLE_LOOP_FILTER_ACROSS_SLICES | None |
deblocking_filter_control_present_flag | 1 | None |
deblocking_filter_override_enabled_flag | 0 | None |
pps_deblocking_filter_disabled_flag | 0 | None |
pps_beta_offset_div2 | 0 | None |
pps_tc_offset_div2 | 0 | None |
pps_scaling_list_data_present_flag | 0 | None |
lists_modification_present_flag | 1 if sending down D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_HEVC lists modifications. Otherwise set as 0. | None | 
log2_parallel_merge_level_minus2 | 0 | None |
slice_segment_header_extension_present_flag | 0 | None |
pps_extension_flag | 0 | None |

## -see-also

