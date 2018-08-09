---
UID: NS:d3d10effect._D3D10_EFFECT_SHADER_DESC
title: "_D3D10_EFFECT_SHADER_DESC"
author: windows-sdk-content
description: Describes an effect shader.
old-location: direct3d10\d3d10_effect_shader_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_shader_desc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 7f99dca9-036c-f8a6-79ea-5316af7e1124, D3D10_EFFECT_SHADER_DESC, D3D10_EFFECT_SHADER_DESC structure [Direct3D 10], _D3D10_EFFECT_SHADER_DESC, d3d10effect/D3D10_EFFECT_SHADER_DESC, direct3d10.d3d10_effect_shader_desc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_EFFECT_SHADER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_EFFECT_SHADER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_EFFECT_SHADER_DESC structure


## -description


Describes an effect shader.


## -struct-fields




### -field pInputSignature

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Passed into CreateInputLayout. Only valid on a vertex shader or geometry shader. See <a href="https://msdn.microsoft.com/61516e1a-f588-4dcb-9ada-9b483fe7cc99">ID3D10Device_CreateInputLayout</a>.


### -field IsInline

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> is the shader is defined inline; otherwise <b>FALSE</b>.


### -field pBytecode

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

A pointer to the compiled shader.


### -field BytecodeLength

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The length of pBytecode.


### -field SODecl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that constains a declaration of the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">stream output </a> from a geometry shader.


### -field NumInputSignatureEntries

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of entries in the input signature.


### -field NumOutputSignatureEntries

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of entries in the output signature.


## -remarks



To get an effect-shader description, call <a href="https://msdn.microsoft.com/5655273a-fc95-4ced-a76f-df622a70745c">ID3D10EffectShaderVariable::GetShaderDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbd69b4b-d2f4-471f-a607-328f5fc603b5">Effect Structures (Direct3D 10)</a>
 

 

