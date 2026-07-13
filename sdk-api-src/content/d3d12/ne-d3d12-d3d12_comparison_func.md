---
UID: NE:d3d12.D3D12_COMPARISON_FUNC
title: D3D12_COMPARISON_FUNC (d3d12.h)
description: Specifies comparison options.
helpviewer_keywords: ["D3D12_COMPARISON_FUNC","D3D12_COMPARISON_FUNC enumeration","D3D12_COMPARISON_FUNC_ALWAYS","D3D12_COMPARISON_FUNC_EQUAL","D3D12_COMPARISON_FUNC_GREATER","D3D12_COMPARISON_FUNC_GREATER_EQUAL","D3D12_COMPARISON_FUNC_LESS","D3D12_COMPARISON_FUNC_LESS_EQUAL","D3D12_COMPARISON_FUNC_NEVER","D3D12_COMPARISON_FUNC_NOT_EQUAL","d3d12/D3D12_COMPARISON_FUNC","d3d12/D3D12_COMPARISON_FUNC_ALWAYS","d3d12/D3D12_COMPARISON_FUNC_EQUAL","d3d12/D3D12_COMPARISON_FUNC_GREATER","d3d12/D3D12_COMPARISON_FUNC_GREATER_EQUAL","d3d12/D3D12_COMPARISON_FUNC_LESS","d3d12/D3D12_COMPARISON_FUNC_LESS_EQUAL","d3d12/D3D12_COMPARISON_FUNC_NEVER","d3d12/D3D12_COMPARISON_FUNC_NOT_EQUAL","direct3d12.d3d12_comparison_func"]
old-location: direct3d12\d3d12_comparison_func.htm
tech.root: direct3d12
ms.assetid: 68223746-59B3-4FDD-B7EF-44557F1C46E3
ms.date: 12/05/2018
ms.keywords: D3D12_COMPARISON_FUNC, D3D12_COMPARISON_FUNC enumeration, D3D12_COMPARISON_FUNC_ALWAYS, D3D12_COMPARISON_FUNC_EQUAL, D3D12_COMPARISON_FUNC_GREATER, D3D12_COMPARISON_FUNC_GREATER_EQUAL, D3D12_COMPARISON_FUNC_LESS, D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_COMPARISON_FUNC_NEVER, D3D12_COMPARISON_FUNC_NOT_EQUAL, d3d12/D3D12_COMPARISON_FUNC, d3d12/D3D12_COMPARISON_FUNC_ALWAYS, d3d12/D3D12_COMPARISON_FUNC_EQUAL, d3d12/D3D12_COMPARISON_FUNC_GREATER, d3d12/D3D12_COMPARISON_FUNC_GREATER_EQUAL, d3d12/D3D12_COMPARISON_FUNC_LESS, d3d12/D3D12_COMPARISON_FUNC_LESS_EQUAL, d3d12/D3D12_COMPARISON_FUNC_NEVER, d3d12/D3D12_COMPARISON_FUNC_NOT_EQUAL, direct3d12.d3d12_comparison_func
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
req.typenames: D3D12_COMPARISON_FUNC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMPARISON_FUNC
 - d3d12/D3D12_COMPARISON_FUNC
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
 - D3D12_COMPARISON_FUNC
---

# D3D12_COMPARISON_FUNC enumeration


## -description

Specifies comparison options.

## -enum-fields

### -field D3D12_COMPARISON_FUNC_NEVER:1

Never pass the comparison.

### -field D3D12_COMPARISON_FUNC_LESS:2

If the source data is less than the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_EQUAL:3

If the source data is equal to the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_LESS_EQUAL:4

If the source data is less than or equal to the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_GREATER:5

If the source data is greater than the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_NOT_EQUAL:6

If the source data is not equal to the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_GREATER_EQUAL:7

If the source data is greater than or equal to the destination data, the comparison passes.

### -field D3D12_COMPARISON_FUNC_ALWAYS:8

Always pass the comparison.

## -remarks

A comparison option determines how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for <ul>
<li>a depth-stencil buffer (<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a>)
            </li>
<li>depth-stencil operations (<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc">D3D12_DEPTH_STENCILOP_DESC</a>)
            </li>
<li>sampler state (<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a>)
            </li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-depth-stencil-desc">CD3DX12_DEPTH_STENCIL_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
