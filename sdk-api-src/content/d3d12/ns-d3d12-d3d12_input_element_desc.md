---
UID: NS:d3d12.D3D12_INPUT_ELEMENT_DESC
title: D3D12_INPUT_ELEMENT_DESC (d3d12.h)
description: Describes a single element for the input-assembler stage of the graphics pipeline.
helpviewer_keywords: ["D3D12_INPUT_ELEMENT_DESC","D3D12_INPUT_ELEMENT_DESC structure","d3d12/D3D12_INPUT_ELEMENT_DESC","direct3d12.d3d12_input_element_desc"]
old-location: direct3d12\d3d12_input_element_desc.htm
tech.root: direct3d12
ms.assetid: FDE49FD5-9F7D-4A57-9AE9-F167AF39B06C
ms.date: 12/05/2018
ms.keywords: D3D12_INPUT_ELEMENT_DESC, D3D12_INPUT_ELEMENT_DESC structure, d3d12/D3D12_INPUT_ELEMENT_DESC, direct3d12.d3d12_input_element_desc
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
req.typenames: D3D12_INPUT_ELEMENT_DESC
req.redist:
ms.custom: 19H1
f1_keywords:
 - D3D12_INPUT_ELEMENT_DESC
 - d3d12/D3D12_INPUT_ELEMENT_DESC
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
 - D3D12_INPUT_ELEMENT_DESC
---

# D3D12_INPUT_ELEMENT_DESC structure


## -description

Describes a single element for the input-assembler stage of the graphics pipeline.

## -struct-fields

### -field SemanticName

The HLSL semantic associated with this element in a shader input-signature. See <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-semantics">HLSL Semantics</a> for more info.

### -field SemanticIndex

The semantic index for the element. A semantic index modifies a semantic, with an integer index number. A semantic index is only needed in a
        case where there is more than one element with the same semantic. For example, a 4x4 matrix would have four components each with the semantic
        name <b>matrix</b>, however each of the four component would have different semantic indices (0, 1, 2, and 3).

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that specifies the format of the element data.

### -field InputSlot

An integer value that identifies the input-assembler. For more info, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">Input Slots</a>. Valid values are between 0 and 15.

### -field AlignedByteOffset

Optional. Offset, in bytes, to this element from the start of the vertex. Use D3D12_APPEND_ALIGNED_ELEMENT (0xffffffff) for convenience to define the current element directly
        after the previous one, including any packing if necessary.

### -field InputSlotClass

A value that identifies the input data class for a single input slot.

### -field InstanceDataStepRate

The number of instances to draw using the same per-instance data before advancing in the buffer by one element. This value must be 0 for an
        element that contains per-vertex data (the slot class is set to the D3D12_INPUT_PER_VERTEX_DATA member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_input_classification">D3D12_INPUT_CLASSIFICATION</a>).

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc">D3D12_INPUT_LAYOUT_DESC</a> structure. A pipeline state object contains a input-layout structure that defines one element being read from an input slot.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
