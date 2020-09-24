---
UID: NS:d3d12.D3D12_DESCRIPTOR_RANGE
title: D3D12_DESCRIPTOR_RANGE (d3d12.h)
description: Describes a descriptor range.
helpviewer_keywords: ["D3D12_DESCRIPTOR_RANGE","D3D12_DESCRIPTOR_RANGE structure","d3d12/D3D12_DESCRIPTOR_RANGE","direct3d12.d3d12_descriptor_range"]
old-location: direct3d12\d3d12_descriptor_range.htm
tech.root: direct3d12
ms.assetid: 6F1C4D05-3E08-4353-B5B9-4C4270FC1403
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_RANGE, D3D12_DESCRIPTOR_RANGE structure, d3d12/D3D12_DESCRIPTOR_RANGE, direct3d12.d3d12_descriptor_range
req.header: d3d12.h
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
req.typenames: D3D12_DESCRIPTOR_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_RANGE
 - d3d12/D3D12_DESCRIPTOR_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DESCRIPTOR_RANGE
---

# D3D12_DESCRIPTOR_RANGE structure


## -description

Describes a descriptor range.

## -struct-fields

### -field RangeType

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type">D3D12_DESCRIPTOR_RANGE_TYPE</a>-typed value that specifies the type of descriptor range.

### -field NumDescriptors

The number of descriptors in the range. Use -1 or UINT_MAX to specify an unbounded size. If a given descriptor range is unbounded, then it must either be the last range in the table definition, or else the following range in the table definition must have a value for *OffsetInDescriptorsFromTableStart* that is not [D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND]().

### -field BaseShaderRegister

The base shader register in the range. For example, for shader-resource views (SRVs), 3 maps to ": register(t3);" in HLSL.

### -field RegisterSpace

The register space. Can typically be 0, but allows multiple descriptor  arrays of unknown size to not appear to overlap.
            For example, for SRVs, by extending the example in the <b>BaseShaderRegister</b> member description, 5 maps to ": register(t3,space5);" in HLSL.

### -field OffsetInDescriptorsFromTableStart

The offset in descriptors, from the start of the descriptor table which was set as the root argument value for this parameter slot. This value can be <b>D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND</b>, which indicates this range should immediately follow the preceding range.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table">D3D12_ROOT_DESCRIPTOR_TABLE</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-descriptor-range">CD3DX12_DESCRIPTOR_RANGE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>