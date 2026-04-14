---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
tech.root: mf
title: D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
ms.date: 04/07/2026
targetos: Windows
description: Contains an opaque quantization map for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
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
 - D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
f1_keywords:
 - D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
 - d3d12video/D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_QUANTIZATION_OPAQUE_MAP
---

## -description

Contains a GPU-resolved quantization map for the current frame to be used instead of the existing CPU buffer pRateControlQPMap parameters. The user must check support for D3D12_FEATURE_VIDEO_ENCODER_QPMAP_INPUT before using this feature.

## -struct-fields

### -field pOpaqueQuantizationMap

Pointer to an ID3D12Resource containing the quantization map. When not NULL, this supersedes the existing CPU buffer pRateControlQPMap picture control structure parameters. Must be first resolved using [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -remarks

## -see-also
