---
UID: NE:d3d12.D3D12_COMPARISON_FUNC
title: D3D12_COMPARISON_FUNC
author: windows-sdk-content
description: Specifies comparison options.
old-location: direct3d12\d3d12_comparison_func.htm
old-project: direct3d12
ms.assetid: 68223746-59B3-4FDD-B7EF-44557F1C46E3
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_COMPARISON_FUNC, D3D12_COMPARISON_FUNC enumeration, D3D12_COMPARISON_FUNC_ALWAYS, D3D12_COMPARISON_FUNC_EQUAL, D3D12_COMPARISON_FUNC_GREATER, D3D12_COMPARISON_FUNC_GREATER_EQUAL, D3D12_COMPARISON_FUNC_LESS, D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_COMPARISON_FUNC_NEVER, D3D12_COMPARISON_FUNC_NOT_EQUAL, d3d12/D3D12_COMPARISON_FUNC, d3d12/D3D12_COMPARISON_FUNC_ALWAYS, d3d12/D3D12_COMPARISON_FUNC_EQUAL, d3d12/D3D12_COMPARISON_FUNC_GREATER, d3d12/D3D12_COMPARISON_FUNC_GREATER_EQUAL, d3d12/D3D12_COMPARISON_FUNC_LESS, d3d12/D3D12_COMPARISON_FUNC_LESS_EQUAL, d3d12/D3D12_COMPARISON_FUNC_NEVER, d3d12/D3D12_COMPARISON_FUNC_NOT_EQUAL, direct3d12.d3d12_comparison_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D12_COMPARISON_FUNC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_COMPARISON_FUNC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_COMPARISON_FUNC enumeration


## -description


Specifies comparison options.


## -enum-fields




### -field D3D12_COMPARISON_FUNC_NEVER

Never pass the comparison.


### -field D3D12_COMPARISON_FUNC_LESS

If the source data is less than the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_EQUAL

If the source data is equal to the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_LESS_EQUAL

If the source data is less than or equal to the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_GREATER

If the source data is greater than the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_NOT_EQUAL

If the source data is not equal to the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_GREATER_EQUAL

If the source data is greater than or equal to the destination data, the comparison passes.


### -field D3D12_COMPARISON_FUNC_ALWAYS

Always pass the comparison.


## -remarks




          A comparison option determines how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for <ul>
<li>
              a depth-stencil buffer (<a href="https://msdn.microsoft.com/C324F6EF-668A-4056-B538-A05329751554">D3D12_DEPTH_STENCIL_DESC</a>)
            </li>
<li>
              depth-stencil operations (<a href="https://msdn.microsoft.com/1E72B486-98E1-4140-80E3-6DF95ECA82DB">D3D12_DEPTH_STENCILOP_DESC</a>)
            </li>
<li>
              sampler state (<a href="https://msdn.microsoft.com/96261FE1-89D4-4135-B5C4-2D788DF4FA12">D3D12_SAMPLER_DESC</a>)
            </li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/D3DB04C3-4564-45A4-830A-E63B8D308B33">CD3DX12_DEPTH_STENCIL_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

