---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
ms.date: 06/13/2021
targetos: Windows
description: Represents the GOP structure for H.264 video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
 - d3d12video/D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264
dev_langs:
 - c++
---

## -description

Represents the GOP structure for H.264 video encoding.

## -struct-fields

### -field GOPLength

The distance between I-frames in the sequence, or the number of pictures on a GOP. If set to 0, only the first frame will be an I frame (infinite GOP).

### -field PPicturePeriod

The period for P-frames to be inserted within the GOP. Note that if GOPLength is set to 0 for infinite GOP, this value must be greater than zero.

Example usage; Let A=GOPLength; B=PPictureInterval

- A=0; B=1 => IPPPPPPPP...
- A=0; B=2 => IBPBPBPBP...
- A=0; B=3 => IBBPBBPBB...
- A=1; B=0 => IIIIIIIII...
- A=2; B=1 => IPIPIPIPI...
- A=3; B=1 => IPPIPPIPP...
- A=3; B=2 => IBPIBPIBP...
- A=4; B=3 => IBBPIBBPIBBP...


### -field pic_order_cnt_type

Specifies the picture order count type filter mode as defined in the H264 standard under pic_order_cnt_type in the sequence parameter set. The value of pic_order_cnt_type shall be in the range of 0 to 2, inclusive.

### -field log2_max_frame_num_minus4

Specifies the value of the variable MaxFrameNum that is used in frame_num related derivations as follows:
MaxFrameNum = 2^(log2_max_frame_num_minus4 + 4)
The value of log2_max_frame_num_minus4 shall be in the range of 0 to 12, inclusive.


### -field log2_max_pic_order_cnt_lsb_minus4

Specifies the value of the variable MaxPicOrderCntLsb that is used in the decoding process for picture order count as specified in clause 8.2.1 as follows:
MaxPicOrderCntLsb = 2^ (log2_max_pic_order_cnt_lsb_minus4 + 4)
The value of log2_max_pic_order_cnt_lsb_minus4 shall be in the range of 0 to 12, inclusive.


## -remarks

## -see-also

