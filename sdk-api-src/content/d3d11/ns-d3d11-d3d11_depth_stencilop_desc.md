---
UID: NS:d3d11.D3D11_DEPTH_STENCILOP_DESC
title: D3D11_DEPTH_STENCILOP_DESC
author: windows-sdk-content
description: Stencil operations that can be performed based on the results of stencil test.
old-location: direct3d11\d3d11_depth_stencilop_desc.htm
tech.root: direct3d11
ms.assetid: 8c375d2f-ecec-4b9f-bd84-625dad53fa6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_DEPTH_STENCILOP_DESC, D3D11_DEPTH_STENCILOP_DESC structure [Direct3D 11], b5c19838-9f15-a711-8c15-008fbca8d2a1, d3d11/D3D11_DEPTH_STENCILOP_DESC, direct3d11.d3d11_depth_stencilop_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_DEPTH_STENCILOP_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_DEPTH_STENCILOP_DESC
req.redist: 
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
 

 

