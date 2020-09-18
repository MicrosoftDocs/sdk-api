---
UID: NS:d3d12.D3D12_DESCRIPTOR_RANGE1
title: D3D12_DESCRIPTOR_RANGE1 (d3d12.h)
description: Describes a descriptor range, with flags to determine their volatility.
helpviewer_keywords: ["D3D12_DESCRIPTOR_RANGE1","D3D12_DESCRIPTOR_RANGE1 structure","d3d12/D3D12_DESCRIPTOR_RANGE1","direct3d12.d3d12_descriptor_range1"]
old-location: direct3d12\d3d12_descriptor_range1.htm
tech.root: direct3d12
ms.assetid: EFC36053-6FD1-4D2E-8214-66B50F0CC0D5
ms.date: 12/05/2018
ms.keywords: D3D12_DESCRIPTOR_RANGE1, D3D12_DESCRIPTOR_RANGE1 structure, d3d12/D3D12_DESCRIPTOR_RANGE1, direct3d12.d3d12_descriptor_range1
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
req.typenames: D3D12_DESCRIPTOR_RANGE1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DESCRIPTOR_RANGE1
 - d3d12/D3D12_DESCRIPTOR_RANGE1
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
 - D3D12_DESCRIPTOR_RANGE1
---

# D3D12_DESCRIPTOR_RANGE1 structure


## -description

Describes a descriptor range, with flags to determine their volatility.

## -struct-fields

### -field RangeType

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type">D3D12_DESCRIPTOR_RANGE_TYPE</a>-typed value that specifies the type of descriptor range.

### -field NumDescriptors

The number of descriptors in the range. Use -1 or UINT_MAX to specify unbounded size. Only the last entry in a table can have unbounded size.

### -field BaseShaderRegister

The base shader register in the range. For example, for shader-resource views (SRVs), 3 maps to ": register(t3);" in HLSL.

### -field RegisterSpace

The register space. Can typically be 0, but allows multiple descriptor  arrays of unknown size to not appear to overlap.
            For example, for SRVs, by extending the example in the <b>BaseShaderRegister</b> member description, 5 maps to ": register(t3,space5);" in HLSL.

### -field Flags

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags">D3D12_DESCRIPTOR_RANGE_FLAGS</a> that determine descriptor and data volatility.

### -field OffsetInDescriptorsFromTableStart

The offset in descriptors from the start of the root signature. This value can be <b>D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND</b>, which indicates this range should immediately follow the preceding range.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1">D3D12_ROOT_DESCRIPTOR_TABLE1</a> structure.
      

Refer to the helper structure <a href="/windows/desktop/direct3d12/cd3dx12-descriptor-range1">CD3DX12_DESCRIPTOR_RANGE1</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>