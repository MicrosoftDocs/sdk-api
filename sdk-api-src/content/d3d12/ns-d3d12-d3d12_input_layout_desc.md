---
UID: NS:d3d12.D3D12_INPUT_LAYOUT_DESC
title: D3D12_INPUT_LAYOUT_DESC (d3d12.h)
description: Describes the input-buffer data for the input-assembler stage.
helpviewer_keywords: ["D3D12_INPUT_LAYOUT_DESC","D3D12_INPUT_LAYOUT_DESC structure","d3d12/D3D12_INPUT_LAYOUT_DESC","direct3d12.d3d12_input_layout_desc"]
old-location: direct3d12\d3d12_input_layout_desc.htm
tech.root: direct3d12
ms.assetid: 44C53830-AE80-402A-808C-2063011711A2
ms.date: 12/05/2018
ms.keywords: D3D12_INPUT_LAYOUT_DESC, D3D12_INPUT_LAYOUT_DESC structure, d3d12/D3D12_INPUT_LAYOUT_DESC, direct3d12.d3d12_input_layout_desc
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
req.typenames: D3D12_INPUT_LAYOUT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_INPUT_LAYOUT_DESC
 - d3d12/D3D12_INPUT_LAYOUT_DESC
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
 - D3D12_INPUT_LAYOUT_DESC
---

# D3D12_INPUT_LAYOUT_DESC structure


## -description

Describes the input-buffer data for the input-assembler stage.

## -struct-fields

### -field pInputElementDescs

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc">D3D12_INPUT_ELEMENT_DESC</a> structures that describe the data types of the input-assembler stage.

### -field NumElements

The number of input-data types in the array of input elements that the <b>pInputElementDescs</b> member points to.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>