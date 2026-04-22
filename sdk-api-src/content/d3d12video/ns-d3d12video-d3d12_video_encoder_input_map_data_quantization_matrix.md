---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
tech.root: mf
title: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
ms.date: 04/07/2026
targetos: Windows
description: Contains quantization matrix input data for the ResolveInputParamLayout operation.
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
req.typenames: D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
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
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
f1_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
 - d3d12video/D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_INPUT_MAP_DATA_QUANTIZATION_MATRIX
---

## -description

Contains quantization matrix input data for [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -struct-fields

### -field pQuantizationMap

Pointer to an ID3D12Resource texture with format DXGI_FORMAT_R8_SINT for H264 and HEVC, or DXGI_FORMAT_R16_SINT for AV1. The dimensions must correspond with the driver-supported QP Map region block size and the current frame resolution, where each (x, y) position on this texture corresponds to the QP value used on that block.

## -remarks

QPMap width is calculated as `(align(FrameResolution.Width, BlockSize) / BlockSize)` and height as `(align(FrameResolution.Height, BlockSize) / BlockSize)`.

For codecs and configurations where QP ranges can be negative, the ranges used by pQuantizationMap as an absolute map are kept in the native signed range. For example, for HEVC the range is [0, 51] for 8-bit pixel depth, [-12, 51] for 10-bit, and similar for higher bit depths.

## -see-also
