---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D11_COMPARISON_FUNC enumeration


## -description


Comparison options.


## -enum-fields




### -field D3D11_COMPARISON_NEVER

Never pass the comparison.


### -field D3D11_COMPARISON_LESS

If the source data is less than the destination data, the comparison passes.


### -field D3D11_COMPARISON_EQUAL

If the source data is equal to the destination data, the comparison passes.


### -field D3D11_COMPARISON_LESS_EQUAL

If the source data is less than or equal to the destination data, the comparison passes.


### -field D3D11_COMPARISON_GREATER

If the source data is greater than the destination data, the comparison passes.


### -field D3D11_COMPARISON_NOT_EQUAL

If the source data is not equal to the destination data, the comparison passes.


### -field D3D11_COMPARISON_GREATER_EQUAL

If the source data is greater than or equal to the destination data, the comparison passes.


### -field D3D11_COMPARISON_ALWAYS

Always pass the comparison.


## -remarks



A comparison option determines whether how the runtime compares source (new) data against destination (existing) data before storing the new data. The comparison option is declared in a description before an object is created. The API allows you to set a comparison option for a depth-stencil buffer (see <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a>), depth-stencil operations (see <a href="https://msdn.microsoft.com/8c375d2f-ecec-4b9f-bd84-625dad53fa6a">D3D11_DEPTH_STENCILOP_DESC</a>), or sampler state (see <a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

