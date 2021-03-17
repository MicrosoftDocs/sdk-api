---
UID: NS:d3d11_1.D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK
title: D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK (d3d11_1.h)
description: Describes a sub sample mapping block.
helpviewer_keywords: ["D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK","D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK structure [Media Foundation]","d3d11_1/D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK","mf.d3d11_video_decoder_sub_sample_mapping_block"]
old-location: mf\d3d11_video_decoder_sub_sample_mapping_block.htm
tech.root: mf
ms.assetid: 82EC2598-60FB-4800-A001-0CCC2D0D529E
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK, D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK structure [Media Foundation], d3d11_1/D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK, mf.d3d11_video_decoder_sub_sample_mapping_block
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK
 - d3d11_1/D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK
---

# D3D11_VIDEO_DECODER_SUB_SAMPLE_MAPPING_BLOCK structure


## -description

Describes a sub sample mapping block.

## -struct-fields

### -field ClearSize

The number of clear (non-encrypted) bytes at the start of the block.

### -field EncryptedSize

The number of encrypted bytes following the clear bytes.

## -remarks

Values in the sub sample mapping blocks are relative to the start of the decode buffer.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>