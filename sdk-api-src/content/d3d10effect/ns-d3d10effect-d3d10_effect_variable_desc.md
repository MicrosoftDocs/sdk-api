---
UID: NS:d3d10effect._D3D10_EFFECT_VARIABLE_DESC
title: D3D10_EFFECT_VARIABLE_DESC (d3d10effect.h)
author: windows-sdk-content
description: Describes an effect variable.
old-location: direct3d10\d3d10_effect_variable_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_variable_desc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10_EFFECT_VARIABLE_DESC, D3D10_EFFECT_VARIABLE_DESC structure [Direct3D 10], d3d10effect/D3D10_EFFECT_VARIABLE_DESC, direct3d10.d3d10_effect_variable_desc, e24d998a-d966-5f94-eabb-5d6535c0928a
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
 - D3D10_EFFECT_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_EFFECT_VARIABLE_DESC
req.redist: 
---

# D3D10_EFFECT_VARIABLE_DESC structure


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

Optional <a href="https://msdn.microsoft.com/en-us/library/Bb205176(v=VS.85).aspx">flags</a> for effect variables.
			


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



To get an effect-variable description, call <a href="https://msdn.microsoft.com/en-us/library/Bb173738(v=VS.85).aspx">ID3D10EffectVariable::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205180(v=VS.85).aspx">Effect Structures (Direct3D 10)</a>
 

 

