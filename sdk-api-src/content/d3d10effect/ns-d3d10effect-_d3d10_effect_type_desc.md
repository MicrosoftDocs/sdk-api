---
UID: NS:d3d10effect._D3D10_EFFECT_TYPE_DESC
title: "_D3D10_EFFECT_TYPE_DESC"
author: windows-sdk-content
description: Describes an effect-variable type.
old-location: direct3d10\d3d10_effect_type_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_type_desc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 18816cca-f97e-a1fe-114c-9342ac218237, D3D10_EFFECT_TYPE_DESC, D3D10_EFFECT_TYPE_DESC structure [Direct3D 10], _D3D10_EFFECT_TYPE_DESC, d3d10effect/D3D10_EFFECT_TYPE_DESC, direct3d10.d3d10_effect_type_desc
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
req.typenames: D3D10_EFFECT_TYPE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_EFFECT_TYPE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_EFFECT_TYPE_DESC structure


## -description


Describes an effect-variable type.


## -struct-fields




### -field TypeName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that contains the variable name.


### -field Class

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172440(v=VS.85).aspx">D3D10_SHADER_VARIABLE_CLASS</a></b>

The variable class (see <a href="https://msdn.microsoft.com/en-us/library/Bb172440(v=VS.85).aspx">D3D10_SHADER_VARIABLE_CLASS</a>).


### -field Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172443(v=VS.85).aspx">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type (see <a href="https://msdn.microsoft.com/en-us/library/Bb172443(v=VS.85).aspx">D3D10_SHADER_VARIABLE_TYPE</a>).


### -field Elements

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements if the variable is an array; otherwise 0.


### -field Members

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of members if the variable is a structure; otherwise 0.


### -field Rows

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rows if the variable is a matrix; otherwise 0.


### -field Columns

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of columns if the variable is a matrix; otherwise 0.


### -field PackedSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes that the variable consumes when it is packed tightly by the compiler.


### -field UnpackedSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes that the variable consumes before it is packed by the compiler.


### -field Stride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes between elements.


## -remarks



To get an effect-variable type, call <a href="https://msdn.microsoft.com/en-us/library/Bb173717(v=VS.85).aspx">ID3D10EffectType::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205180(v=VS.85).aspx">Effect Structures (Direct3D 10)</a>
 

 

