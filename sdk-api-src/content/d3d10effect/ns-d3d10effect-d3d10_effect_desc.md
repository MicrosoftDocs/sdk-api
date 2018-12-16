---
UID: NS:d3d10effect._D3D10_EFFECT_DESC
title: D3D10_EFFECT_DESC
author: windows-sdk-content
description: Describes an effect.
old-location: direct3d10\d3d10_effect_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_desc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 1f8c640b-441a-ed00-b882-58a32c647df9, D3D10_EFFECT_DESC, D3D10_EFFECT_DESC structure [Direct3D 10], d3d10effect/D3D10_EFFECT_DESC, direct3d10.d3d10_effect_desc
ms.topic: struct
req.header: d3d10effect.h
req.include-header: D3D10.h
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
 - d3d10effect.h
api_name:
 - D3D10_EFFECT_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_EFFECT_DESC
req.redist: 
---

# D3D10_EFFECT_DESC structure


## -description


Describes an effect.


## -struct-fields




### -field IsChildEffect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the effect is a <a href="https://msdn.microsoft.com/9f029be5-4ce0-46ca-909b-adaa980398e7">child effect</a>; otherwise <b>FALSE</b>.


### -field ConstantBuffers

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of constant buffers.


### -field SharedConstantBuffers

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of constant buffers shared in an effect pool.


### -field GlobalVariables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of global variables.


### -field SharedGlobalVariables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of global variables shared in an effect pool.


### -field Techniques

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of techniques.


## -remarks



To get an effect description, call <a href="https://msdn.microsoft.com/bc8add27-778b-416e-a031-d5861ec79b90">ID3D10Effect::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbd69b4b-d2f4-471f-a607-328f5fc603b5">Effect Structures (Direct3D 10)</a>
 

 

