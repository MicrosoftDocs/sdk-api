---
UID: NS:d3d12.D3D12_RESOURCE_DESC1
title: D3D12_RESOURCE_DESC1 (d3d12.h)
description: Describes a resource, such as a texture, including a mip region. This structure is used in several methods.
helpviewer_keywords: ["D3D12_RESOURCE_DESC1","D3D12_RESOURCE_DESC1 structure","d3d12/D3D12_RESOURCE_DESC1","direct3d12.d3d12_resource_desc1"]
tech.root: direct3d12
ms.date: 09/16/2020
ms.keywords: D3D12_RESOURCE_DESC1, D3D12_RESOURCE_DESC1 structure, d3d12/D3D12_RESOURCE_DESC1, direct3d12.d3d12_resource_desc1
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D3D12_RESOURCE_DESC1
req.redist: 
f1_keywords:
 - D3D12_RESOURCE_DESC1
 - d3d12/D3D12_RESOURCE_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RESOURCE_DESC1
---

## -description

Describes a resource, such as a texture, including a mip region. This structure is used in several methods.

## -struct-fields

### -field Dimension

One member of <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>, specifying the dimensions of the resource (for example, D3D12_RESOURCE_DIMENSION_TEXTURE1D), or whether it is a buffer ((D3D12_RESOURCE_DIMENSION_BUFFER).

### -field Alignment

Specifies the alignment.

### -field Width

Specifies the width of the resource.

### -field Height

Specifies the height of the resource.

### -field DepthOrArraySize

Specifies the depth of the resource, if it is 3D, or the array size if it is an array of 1D or 2D resources.

### -field MipLevels

Specifies the number of MIP levels.

### -field Format

Specifies one member of <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>.

### -field SampleDesc

Specifies a <a href="/windows/win32/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a> structure.

### -field Layout

Specifies one member of <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT</a>.

### -field Flags

Bitwise-OR'd flags, as <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAGS</a> enumeration constants.

### -field SamplerFeedbackMipRegion

A [D3D12_MIP_REGION](./ns-d3d12-d3d12_mip_region.md) struct.

## -remarks

For remarks, see [D3D12_RESOURCE_DESC](./ns-d3d12-d3d12_resource_desc.md).

## -see-also

* <a href="/windows/win32/direct3d12/direct3d-12-structures">Core structures</a>

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
