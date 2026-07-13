---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAGS
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAGS
ms.date: 07/07/2021
targetos: Windows
description: Specifies errors encountered during the ID3D12VideoEncodeCommandList2::EncodeFrame operation.
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
 - D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAGS
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAGS
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAGS
dev_langs:
 - c++
---

## -description

Specifies errors encountered during the [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) operation.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_NO_ERROR

No error.

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_CODEC_PICTURE_CONTROL_NOT_SUPPORTED

Specified codec picture control not supported.

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_SUBREGION_LAYOUT_CONFIGURATION_NOT_SUPPORTED

Specified subregion layout subregion not supported.

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_INVALID_REFERENCE_PICTURES

Invalid reference pictures provided.

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_RECONFIGURATION_REQUEST_NOT_SUPPORTED

Reconfiguration request is unsupported.

### -field D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG_INVALID_METADATA_BUFFER_SOURCE

Invalid metadata buffer source.

## -remarks

## -see-also

