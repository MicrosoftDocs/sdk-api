---
UID: NS:d3d10effect._D3D10_EFFECT_VARIABLE_DESC
title: "_D3D10_EFFECT_VARIABLE_DESC"
author: windows-sdk-content
description: Describes an effect variable.
old-location: direct3d10\d3d10_effect_variable_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_variable_desc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_EFFECT_VARIABLE_DESC, D3D10_EFFECT_VARIABLE_DESC structure [Direct3D 10], _D3D10_EFFECT_VARIABLE_DESC, d3d10effect/D3D10_EFFECT_VARIABLE_DESC, direct3d10.d3d10_effect_variable_desc, e24d998a-d966-5f94-eabb-5d6535c0928a
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10effect.h
req.include-header: D3D10.h
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
req.typenames: D3D10_EFFECT_VARIABLE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_EFFECT_VARIABLE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_EFFECT_VARIABLE_DESC structure


## -description


Describes an effect variable.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that contains the variable name.


### -field Semantic

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The semantic attached to the variable; otherwise <b>NULL</b>.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional <a href="https://msdn.microsoft.com/434bcff8-47ea-480d-bc0b-44d3ed1f8cce">flags</a> for effect variables.
			


### -field Annotations

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of annotations; otherwise 0.


### -field BufferOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset between the beginning of the constant buffer and this variable; otherwise 0.


### -field ExplicitBindPoint

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The register that this variable is bound to. To bind a variable explicitly use the D3D10_EFFECT_VARIABLE_EXPLICIT_BIND_POINT flag.


## -remarks



To get an effect-variable description, call <a href="https://msdn.microsoft.com/64ab5d84-834b-49cf-a873-6c249d808662">ID3D10EffectVariable::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbd69b4b-d2f4-471f-a607-328f5fc603b5">Effect Structures (Direct3D 10)</a>
 

 

