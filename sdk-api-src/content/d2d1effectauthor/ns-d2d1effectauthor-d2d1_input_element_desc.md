---
UID: NS:d2d1effectauthor.D2D1_INPUT_ELEMENT_DESC
title: D2D1_INPUT_ELEMENT_DESC (d2d1effectauthor.h)
description: A description of a single element to the vertex layout.
helpviewer_keywords: ["D2D1_INPUT_ELEMENT_DESC","D2D1_INPUT_ELEMENT_DESC structure [Direct2D]","d2d1effectauthor/D2D1_INPUT_ELEMENT_DESC","direct2d.d2d1_input_element_desc"]
old-location: direct2d\d2d1_input_element_desc.htm
tech.root: Direct2D
ms.assetid: 17e70872-f0cb-4f9d-8188-d6d24770db04
ms.date: 12/05/2018
ms.keywords: D2D1_INPUT_ELEMENT_DESC, D2D1_INPUT_ELEMENT_DESC structure [Direct2D], d2d1effectauthor/D2D1_INPUT_ELEMENT_DESC, direct2d.d2d1_input_element_desc
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_INPUT_ELEMENT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_INPUT_ELEMENT_DESC
 - d2d1effectauthor/D2D1_INPUT_ELEMENT_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_INPUT_ELEMENT_DESC
---

# D2D1_INPUT_ELEMENT_DESC structure


## -description

A description of a single element to the vertex layout.

## -struct-fields

### -field semanticName

The <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">HLSL semantic</a> associated with this element in a <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-signatures">shader input-signature</a>.

### -field semanticIndex

The semantic index for the element. A semantic index modifies a semantic, with an integer index number. A semantic index is only needed in a case where there is more than one element with the same semantic. For example, a 4x4 matrix would have four components each with the semantic name matrix; however, each of the four components would have different semantic indices (0, 1, 2, and 3).

### -field format

The data type of the element data.

### -field inputSlot

An integer value that identifies the input-assembler. Valid values are between 0 and 15.

### -field alignedByteOffset

The offset in bytes between each element.

## -remarks

This structure is a subset of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc">D3D11_INPUT_ELEMENT_DESC</a> that omits fields required to define a vertex layout.

If the <a href="/windows/desktop/Direct2D/direct2d-constants">D2D1_APPEND_ALIGNED_ELEMENT</a> constant is used for  <b>alignedByteOffset</b>, the elements will be packed contiguously for convenience.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_vertex_usage">D2D1_VERTEX_USAGE</a>



<a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">Getting Started with the Input-Assembler Stage</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">ID2D1EffectContext::LoadVertexShader</a>



<a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">Semantics</a>



<a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-signatures">Signatures</a>