---
UID: NE:d3d10.D3D10_COMPARISON_FUNC
title: D3D10_COMPARISON_FUNC
author: windows-sdk-content
description: Comparison options.
old-location: direct3d10\d3d10_comparison_func.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_comparison_func.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 5efee8e5-417a-75e5-2f53-291d2450fa5f, D3D10_COMPARISON_ALWAYS, D3D10_COMPARISON_EQUAL, D3D10_COMPARISON_FUNC, D3D10_COMPARISON_FUNC enumeration [Direct3D 10], D3D10_COMPARISON_GREATER, D3D10_COMPARISON_GREATER_EQUAL, D3D10_COMPARISON_LESS, D3D10_COMPARISON_LESS_EQUAL, D3D10_COMPARISON_NEVER, D3D10_COMPARISON_NOT_EQUAL, d3d10/D3D10_COMPARISON_ALWAYS, d3d10/D3D10_COMPARISON_EQUAL, d3d10/D3D10_COMPARISON_FUNC, d3d10/D3D10_COMPARISON_GREATER, d3d10/D3D10_COMPARISON_GREATER_EQUAL, d3d10/D3D10_COMPARISON_LESS, d3d10/D3D10_COMPARISON_LESS_EQUAL, d3d10/D3D10_COMPARISON_NEVER, d3d10/D3D10_COMPARISON_NOT_EQUAL, direct3d10.d3d10_comparison_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_COMPARISON_FUNC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_COMPARISON_FUNC
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
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



A comparison option determines whether how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for a depth-stencil buffer (see <a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a>), depth-stencil operations (see <a href="https://msdn.microsoft.com/d7fac8af-cd84-4aae-9e62-d5394e79f53c">D3D10_DEPTH_STENCILOP_DESC</a>), or sampler state (see <a href="https://msdn.microsoft.com/b97db311-de57-45f3-a6dd-8af768b2680d">D3D10_SAMPLER_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

