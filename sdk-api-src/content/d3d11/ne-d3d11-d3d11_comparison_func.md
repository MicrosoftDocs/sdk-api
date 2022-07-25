---
UID: NE:d3d11.D3D11_COMPARISON_FUNC
title: D3D11_COMPARISON_FUNC (d3d11.h)
description: Comparison options.
helpviewer_keywords: ["6fbaba9a-9ef4-f12b-ab05-adee47e72652","D3D11_COMPARISON_ALWAYS","D3D11_COMPARISON_EQUAL","D3D11_COMPARISON_FUNC","D3D11_COMPARISON_FUNC enumeration [Direct3D 11]","D3D11_COMPARISON_GREATER","D3D11_COMPARISON_GREATER_EQUAL","D3D11_COMPARISON_LESS","D3D11_COMPARISON_LESS_EQUAL","D3D11_COMPARISON_NEVER","D3D11_COMPARISON_NOT_EQUAL","d3d11/D3D11_COMPARISON_ALWAYS","d3d11/D3D11_COMPARISON_EQUAL","d3d11/D3D11_COMPARISON_FUNC","d3d11/D3D11_COMPARISON_GREATER","d3d11/D3D11_COMPARISON_GREATER_EQUAL","d3d11/D3D11_COMPARISON_LESS","d3d11/D3D11_COMPARISON_LESS_EQUAL","d3d11/D3D11_COMPARISON_NEVER","d3d11/D3D11_COMPARISON_NOT_EQUAL","direct3d11.d3d11_comparison_func"]
old-location: direct3d11\d3d11_comparison_func.htm
tech.root: direct3d11
ms.assetid: 3546c7b8-ae25-4554-85e2-527433a74a94
ms.date: 12/05/2018
ms.keywords: 6fbaba9a-9ef4-f12b-ab05-adee47e72652, D3D11_COMPARISON_ALWAYS, D3D11_COMPARISON_EQUAL, D3D11_COMPARISON_FUNC, D3D11_COMPARISON_FUNC enumeration [Direct3D 11], D3D11_COMPARISON_GREATER, D3D11_COMPARISON_GREATER_EQUAL, D3D11_COMPARISON_LESS, D3D11_COMPARISON_LESS_EQUAL, D3D11_COMPARISON_NEVER, D3D11_COMPARISON_NOT_EQUAL, d3d11/D3D11_COMPARISON_ALWAYS, d3d11/D3D11_COMPARISON_EQUAL, d3d11/D3D11_COMPARISON_FUNC, d3d11/D3D11_COMPARISON_GREATER, d3d11/D3D11_COMPARISON_GREATER_EQUAL, d3d11/D3D11_COMPARISON_LESS, d3d11/D3D11_COMPARISON_LESS_EQUAL, d3d11/D3D11_COMPARISON_NEVER, d3d11/D3D11_COMPARISON_NOT_EQUAL, direct3d11.d3d11_comparison_func
req.header: d3d11.h
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
req.typenames: D3D11_COMPARISON_FUNC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_COMPARISON_FUNC
 - d3d11/D3D11_COMPARISON_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_COMPARISON_FUNC
---

# D3D11_COMPARISON_FUNC enumeration


## -description

Comparison options.

## -enum-fields

### -field D3D11_COMPARISON_NEVER:1

Never pass the comparison.

### -field D3D11_COMPARISON_LESS:2

If the source data is less than the destination data, the comparison passes.

### -field D3D11_COMPARISON_EQUAL:3

If the source data is equal to the destination data, the comparison passes.

### -field D3D11_COMPARISON_LESS_EQUAL:4

If the source data is less than or equal to the destination data, the comparison passes.

### -field D3D11_COMPARISON_GREATER:5

If the source data is greater than the destination data, the comparison passes.

### -field D3D11_COMPARISON_NOT_EQUAL:6

If the source data is not equal to the destination data, the comparison passes.

### -field D3D11_COMPARISON_GREATER_EQUAL:7

If the source data is greater than or equal to the destination data, the comparison passes.

### -field D3D11_COMPARISON_ALWAYS:8

Always pass the comparison.

## -remarks

A comparison option determines whether how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for a depth-stencil buffer (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>), depth-stencil operations (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencilop_desc">D3D11_DEPTH_STENCILOP_DESC</a>), or sampler state (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc">D3D11_SAMPLER_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
