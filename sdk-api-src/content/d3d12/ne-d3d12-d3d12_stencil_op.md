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

# D3D12_STENCIL_OP enumeration


## -description


Identifies the stencil operations that can be performed during depth-stencil testing.


## -enum-fields




### -field D3D12_STENCIL_OP_KEEP

Keep the existing stencil data.


### -field D3D12_STENCIL_OP_ZERO

Set the stencil data to 0.


### -field D3D12_STENCIL_OP_REPLACE

Set the stencil data to the reference value set by calling <a href="https://msdn.microsoft.com/cd5642c4-8bbe-4b5d-9f04-87de82ee9601">ID3D11DeviceContext::OMSetDepthStencilState</a>.


### -field D3D12_STENCIL_OP_INCR_SAT

Increment the stencil value by 1, and clamp the result.


### -field D3D12_STENCIL_OP_DECR_SAT

Decrement the stencil value by 1, and clamp the result.


### -field D3D12_STENCIL_OP_INVERT

Invert the stencil data.


### -field D3D12_STENCIL_OP_INCR

Increment the stencil value by 1, and wrap the result if necessary.


### -field D3D12_STENCIL_OP_DECR

Decrement the stencil value by 1, and wrap the result if necessary.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/1E72B486-98E1-4140-80E3-6DF95ECA82DB">D3D12_DEPTH_STENCILOP_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/D3DB04C3-4564-45A4-830A-E63B8D308B33">CD3DX12_DEPTH_STENCIL_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

