---
UID: NS:d3d12.D3D12_INDIRECT_ARGUMENT_DESC
title: D3D12_INDIRECT_ARGUMENT_DESC (d3d12.h)
description: Describes an indirect argument (an indirect parameter), for use with a command signature.
helpviewer_keywords: ["D3D12_INDIRECT_ARGUMENT_DESC","D3D12_INDIRECT_ARGUMENT_DESC structure","d3d12/D3D12_INDIRECT_ARGUMENT_DESC","direct3d12.d3d12_indirect_argument_desc"]
old-location: direct3d12\d3d12_indirect_argument_desc.htm
tech.root: direct3d12
ms.assetid: 2B51E4B1-F48A-4937-A92D-6AE9449018B4
ms.date: 12/05/2018
ms.keywords: D3D12_INDIRECT_ARGUMENT_DESC, D3D12_INDIRECT_ARGUMENT_DESC structure, d3d12/D3D12_INDIRECT_ARGUMENT_DESC, direct3d12.d3d12_indirect_argument_desc
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
req.typenames: D3D12_INDIRECT_ARGUMENT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_INDIRECT_ARGUMENT_DESC
 - d3d12/D3D12_INDIRECT_ARGUMENT_DESC
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
 - D3D12_INDIRECT_ARGUMENT_DESC
---

# D3D12_INDIRECT_ARGUMENT_DESC structure


## -description

Describes an indirect argument (an indirect parameter), for use with a command signature.

## -struct-fields

### -field Type

A single <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type">D3D12_INDIRECT_ARGUMENT_TYPE</a> enumeration constant.

### -field VertexBuffer

### -field VertexBuffer.Slot

Specifies the slot containing the vertex buffer address.

### -field Constant

### -field Constant.RootParameterIndex

Specifies the root index of the constant.

### -field Constant.DestOffsetIn32BitValues

The offset, in 32-bit values, to set the first constant of the group.
                Supports multi-value constants at a given root index.
                Root constant entries must be sorted from smallest to largest DestOffsetIn32BitValues.

### -field Constant.Num32BitValuesToSet

The number of 32-bit constants that are set at the given root index.
                Supports multi-value constants at a given root index.

### -field ConstantBufferView

### -field ConstantBufferView.RootParameterIndex

Specifies the root index of the CBV.

### -field ShaderResourceView

### -field ShaderResourceView.RootParameterIndex

Specifies the root index of the SRV.

### -field UnorderedAccessView

### -field UnorderedAccessView.RootParameterIndex

Specifies the root index of the UAV.

## -remarks

Use this structure with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc">D3D12_COMMAND_SIGNATURE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/example-root-signatures">Example Root Signatures</a>