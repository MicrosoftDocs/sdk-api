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

# D3D11_DEPTH_STENCILOP_DESC structure


## -description


Stencil operations that can be performed based on the results of stencil test.


## -struct-fields




### -field StencilFailOp

Type: <b><a href="https://msdn.microsoft.com/4a08ce69-a3e1-43d3-bf7e-e14b106fbecf">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing fails.


### -field StencilDepthFailOp

Type: <b><a href="https://msdn.microsoft.com/4a08ce69-a3e1-43d3-bf7e-e14b106fbecf">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing passes and depth testing fails.


### -field StencilPassOp

Type: <b><a href="https://msdn.microsoft.com/4a08ce69-a3e1-43d3-bf7e-e14b106fbecf">D3D11_STENCIL_OP</a></b>

The stencil operation to perform when stencil testing and depth testing both pass.


### -field StencilFunc

Type: <b><a href="https://msdn.microsoft.com/3546c7b8-ae25-4554-85e2-527433a74a94">D3D11_COMPARISON_FUNC</a></b>

A function that compares stencil data against existing stencil data. The function options are listed in <a href="https://msdn.microsoft.com/3546c7b8-ae25-4554-85e2-527433a74a94">D3D11_COMPARISON_FUNC</a>.


## -remarks



All stencil operations are specified as a <a href="https://msdn.microsoft.com/4a08ce69-a3e1-43d3-bf7e-e14b106fbecf">D3D11_STENCIL_OP</a>. The stencil operation can be set differently based on the outcome of the stencil test (which is referred to as <b>StencilFunc</b> in the stencil test portion of depth-stencil testing.

This structure is a member of a <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">depth-stencil description</a>. 




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

