---
UID: NS:dxva._DXVA_PicParams_HEVC
title: "_DXVA_PicParams_HEVC"
author: windows-driver-content
description: Provides the picture-level parameters of a compressed picture for HEVC video decoding.
old-location: mf\dxva_picparams_hevc.htm
old-project: medfound
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPDXVA_PicParams_HEVC, DXVA_PicParams_HEVC, DXVA_PicParams_HEVC structure [Media Foundation], PDXVA_PicParams_HEVC, PDXVA_PicParams_HEVC structure pointer [Media Foundation], _DXVA_PicParams_HEVC, dxva/DXVA_PicParams_HEVC, dxva/PDXVA_PicParams_HEVC, mf.dxva_picparams_hevc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVA_PicParams_HEVC, *LPDXVA_PicParams_HEVC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva.h
api_name:
-	DXVA_PicParams_HEVC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_PicParams_HEVC structure


## -description


 Provides the picture-level parameters of a compressed picture for HEVC video decoding. 


## -struct-fields




### -field chroma_format_idc


### -field separate_colour_plane_flag


### -field bit_depth_luma_minus8


### -field bit_depth_chroma_minus8


### -field log2_max_pic_order_cnt_lsb_minus4


### -field NoPicReorderingFlag


### -field NoBiPredFlag


### -field ReservedBits1


### -field scaling_list_enabled_flag


### -field amp_enabled_flag


### -field sample_adaptive_offset_enabled_flag


### -field pcm_enabled_flag


### -field pcm_sample_bit_depth_luma_minus1


### -field pcm_sample_bit_depth_chroma_minus1


### -field log2_min_pcm_luma_coding_block_size_minus3


### -field log2_diff_max_min_pcm_luma_coding_block_size


### -field pcm_loop_filter_disabled_flag


### -field long_term_ref_pics_present_flag


### -field sps_temporal_mvp_enabled_flag


### -field strong_intra_smoothing_enabled_flag


### -field dependent_slice_segments_enabled_flag


### -field output_flag_present_flag


### -field num_extra_slice_header_bits


### -field sign_data_hiding_enabled_flag


### -field cabac_init_present_flag


### -field ReservedBits3


### -field constrained_intra_pred_flag


### -field transform_skip_enabled_flag


### -field cu_qp_delta_enabled_flag


### -field pps_slice_chroma_qp_offsets_present_flag


### -field weighted_pred_flag


### -field weighted_bipred_flag


### -field transquant_bypass_enabled_flag


### -field tiles_enabled_flag


### -field entropy_coding_sync_enabled_flag


### -field uniform_spacing_flag


### -field loop_filter_across_tiles_enabled_flag


### -field pps_loop_filter_across_slices_enabled_flag


### -field deblocking_filter_override_enabled_flag


### -field pps_deblocking_filter_disabled_flag


### -field lists_modification_present_flag


### -field slice_segment_header_extension_present_flag


### -field IrapPicFlag


### -field IdrPicFlag


### -field IntraPicFlag


### -field ReservedBits4


### -field PicWidthInMinCbsY


### -field PicHeightInMinCbsY


### -field CurrPic


### -field sps_max_dec_pic_buffering_minus1


### -field log2_min_luma_coding_block_size_minus3


### -field log2_diff_max_min_luma_coding_block_size


### -field log2_min_transform_block_size_minus2


### -field log2_diff_max_min_transform_block_size


### -field max_transform_hierarchy_depth_inter


### -field max_transform_hierarchy_depth_intra


### -field num_short_term_ref_pic_sets


### -field num_long_term_ref_pics_sps


### -field num_ref_idx_l0_default_active_minus1


### -field num_ref_idx_l1_default_active_minus1


### -field init_qp_minus26


### -field ucNumDeltaPocsOfRefRpsIdx


### -field wNumBitsForShortTermRPSInSlice


### -field ReservedBits2


### -field pps_cb_qp_offset


### -field pps_cr_qp_offset


### -field num_tile_columns_minus1


### -field num_tile_rows_minus1


### -field column_width_minus1


### -field row_height_minus1


### -field diff_cu_qp_delta_depth


### -field pps_beta_offset_div2


### -field pps_tc_offset_div2


### -field log2_parallel_merge_level_minus2


### -field CurrPicOrderCntVal


### -field RefPicList


### -field ReservedBits5


### -field PicOrderCntValList


### -field RefPicSetStCurrBefore


### -field RefPicSetStCurrAfter


### -field RefPicSetLtCurr


### -field ReservedBits6


### -field ReservedBits7


### -field StatusReportFeedbackNumber


#### - dwCodingParamToolFlags


#### - dwCodingSettingPicturePropertyFlags


#### - wFormatAndSequenceInfoFlags


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

