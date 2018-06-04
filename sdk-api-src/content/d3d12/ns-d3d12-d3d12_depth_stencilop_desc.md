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

# D3D12_DEPTH_STENCILOP_DESC structure


## -description


Describes stencil operations that can be performed based on the results of stencil test.


## -struct-fields




### -field StencilFailOp

A <a href="https://msdn.microsoft.com/E3527EA4-D931-49C7-B446-829B93A8A620">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing fails.


### -field StencilDepthFailOp

A <a href="https://msdn.microsoft.com/E3527EA4-D931-49C7-B446-829B93A8A620">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing passes and depth testing fails.


### -field StencilPassOp

A <a href="https://msdn.microsoft.com/E3527EA4-D931-49C7-B446-829B93A8A620">D3D12_STENCIL_OP</a>-typed value that identifies the stencil operation to perform when stencil testing and depth testing both pass.


### -field StencilFunc

A <a href="https://msdn.microsoft.com/68223746-59B3-4FDD-B7EF-44557F1C46E3">D3D12_COMPARISON_FUNC</a>-typed value that identifies the function that compares stencil data against existing stencil data. 


## -remarks



All stencil operations are specified as a <a href="https://msdn.microsoft.com/E3527EA4-D931-49C7-B446-829B93A8A620">D3D12_STENCIL_OP</a>-typed value. Each stencil operation can be set differently based on the outcome of the stencil test, which is referred to as <b>StencilFunc</b>, in the stencil test portion of depth-stencil testing.

Members of <a href="https://msdn.microsoft.com/C324F6EF-668A-4056-B538-A05329751554">D3D12_DEPTH_STENCIL_DESC</a> have this structure for their data type. 




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

