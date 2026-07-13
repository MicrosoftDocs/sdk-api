---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
tech.root: mf
title: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
ms.date: 06/25/2021
targetos: Windows
description: Represents a picture list modification operation for H264 video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
f1_keywords:
 - D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
 - d3d12video/D3D12_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_REFERENCE_PICTURE_LIST_MODIFICATION_OPERATION
dev_langs:
 - c++
---

## -description

Represents a picture list modification operation for H264 video encoding.

## -struct-fields

### -field modification_of_pic_nums_idc

Together with abs_diff_pic_num_minus1 or long_term_pic_num specifies which of the reference pictures are re-mapped. 

### -field abs_diff_pic_num_minus1

Specifies the absolute difference between the picture number of the picture being moved to the current index in the list and the picture number prediction value. 

### -field long_term_pic_num

Specifies the long-term picture number of the picture being moved to the current index in the list. 

## -remarks

For more information, refer to H264 specification for more details: section 7.4.3.1 "Reference picture list modification semantics".
.

## -see-also

