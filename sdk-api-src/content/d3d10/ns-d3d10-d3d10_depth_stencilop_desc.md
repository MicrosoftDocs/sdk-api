---
UID: NS:d3d10.D3D10_DEPTH_STENCILOP_DESC
title: D3D10_DEPTH_STENCILOP_DESC
author: windows-driver-content
description: Describes the stencil operations that can be performed based on the results of stencil test.
old-location: direct3d10\d3d10_depth_stencilop_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_depth_stencilop_desc.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: D3D10_DEPTH_STENCILOP_DESC, D3D10_DEPTH_STENCILOP_DESC structure [Direct3D 10], d3d10/D3D10_DEPTH_STENCILOP_DESC, direct3d10.d3d10_depth_stencilop_desc, f40038a7-1ea3-7c24-dccb-e727b020078f
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D10_DEPTH_STENCILOP_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_DEPTH_STENCILOP_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_DEPTH_STENCILOP_DESC structure


## -description


Describes the stencil operations that can be performed based on the results of <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">stencil test</a>.


## -struct-fields




### -field StencilFailOp

Type: <b><a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a></b>

A member of the <a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing fails. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.


### -field StencilDepthFailOp

Type: <b><a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a></b>

A member of the <a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing passes and depth testing fails. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.


### -field StencilPassOp

Type: <b><a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a></b>

A member of the <a href="https://msdn.microsoft.com/57bbb204-afa9-46a5-b3db-199eb9e41b4f">D3D10_STENCIL_OP</a> enumerated type that describes the stencil operation to perform when stencil testing and depth testing both pass. The default value is <b>D3D10_STENCIL_OP_KEEP</b>.


### -field StencilFunc

Type: <b><a href="https://msdn.microsoft.com/e0d0d421-ebd0-441c-949b-97506703e3fa">D3D10_COMPARISON_FUNC</a></b>

A member of the <a href="https://msdn.microsoft.com/e0d0d421-ebd0-441c-949b-97506703e3fa">D3D10_COMPARISON_FUNC</a> enumerated type that describes how stencil data is compared against existing stencil data. The default value is <b>D3D10_COMPARISON_ALWAYS</b>.


## -remarks



The stencil operation can be set differently based on the outcome of the stencil test by using the <b>StencilFunc</b> member.  This can be done for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">stencil test</a> portion of depth-stencil testing.

The D3D10_DEPTH_STENCILOP_DESC structure is a member of the <a href="https://msdn.microsoft.com/5337bb50-95ce-47cd-bda5-2828bf3f85d0">D3D10_DEPTH_STENCIL_DESC</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

