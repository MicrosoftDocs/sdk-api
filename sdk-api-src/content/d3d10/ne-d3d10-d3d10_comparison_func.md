---
UID: NE:d3d10.D3D10_COMPARISON_FUNC
title: D3D10_COMPARISON_FUNC (d3d10.h)
author: windows-sdk-content
description: Comparison options.
old-location: direct3d10\d3d10_comparison_func.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_comparison_func.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5efee8e5-417a-75e5-2f53-291d2450fa5f, D3D10_COMPARISON_ALWAYS, D3D10_COMPARISON_EQUAL, D3D10_COMPARISON_FUNC, D3D10_COMPARISON_FUNC enumeration [Direct3D 10], D3D10_COMPARISON_GREATER, D3D10_COMPARISON_GREATER_EQUAL, D3D10_COMPARISON_LESS, D3D10_COMPARISON_LESS_EQUAL, D3D10_COMPARISON_NEVER, D3D10_COMPARISON_NOT_EQUAL, d3d10/D3D10_COMPARISON_ALWAYS, d3d10/D3D10_COMPARISON_EQUAL, d3d10/D3D10_COMPARISON_FUNC, d3d10/D3D10_COMPARISON_GREATER, d3d10/D3D10_COMPARISON_GREATER_EQUAL, d3d10/D3D10_COMPARISON_LESS, d3d10/D3D10_COMPARISON_LESS_EQUAL, d3d10/D3D10_COMPARISON_NEVER, d3d10/D3D10_COMPARISON_NOT_EQUAL, direct3d10.d3d10_comparison_func
ms.topic: enum
f1_keywords: 
 - "d3d10/D3D10_COMPARISON_FUNC"
dev_langs:
 - c++
req.header: d3d10.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_COMPARISON_FUNC
targetos: Windows
req.typenames: D3D10_COMPARISON_FUNC
req.redist: 
ms.custom: 19H1
---

# D3D10_COMPARISON_FUNC enumeration


## -description


Comparison options.


## -enum-fields




### -field D3D10_COMPARISON_NEVER

Never pass the comparison.


### -field D3D10_COMPARISON_LESS

If the source data is less than the destination data, the comparison passes.


### -field D3D10_COMPARISON_EQUAL

If the source data is equal to the destination data, the comparison passes.


### -field D3D10_COMPARISON_LESS_EQUAL

If the source data is less than or equal to the destination data, the comparison passes.


### -field D3D10_COMPARISON_GREATER

If the source data is greater than the destination data, the comparison passes.


### -field D3D10_COMPARISON_NOT_EQUAL

If the source data is not equal to the destination data, the comparison passes.


### -field D3D10_COMPARISON_GREATER_EQUAL

If the source data is greater than or equal to the destination data, the comparison passes.


### -field D3D10_COMPARISON_ALWAYS

Always pass the comparison.


## -remarks



A comparison option determines whether how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for a depth-stencil buffer (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_desc">D3D10_DEPTH_STENCIL_DESC</a>), depth-stencil operations (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencilop_desc">D3D10_DEPTH_STENCILOP_DESC</a>), or sampler state (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc">D3D10_SAMPLER_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

