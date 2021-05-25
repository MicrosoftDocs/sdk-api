---
UID: NS:d3d10effect._D3D10_EFFECT_SHADER_DESC
title: D3D10_EFFECT_SHADER_DESC (d3d10effect.h)
description: Describes an effect shader.
helpviewer_keywords: ["7f99dca9-036c-f8a6-79ea-5316af7e1124","D3D10_EFFECT_SHADER_DESC","D3D10_EFFECT_SHADER_DESC structure [Direct3D 10]","d3d10effect/D3D10_EFFECT_SHADER_DESC","direct3d10.d3d10_effect_shader_desc"]
old-location: direct3d10\d3d10_effect_shader_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_shader_desc.htm
ms.date: 12/05/2018
ms.keywords: 7f99dca9-036c-f8a6-79ea-5316af7e1124, D3D10_EFFECT_SHADER_DESC, D3D10_EFFECT_SHADER_DESC structure [Direct3D 10], d3d10effect/D3D10_EFFECT_SHADER_DESC, direct3d10.d3d10_effect_shader_desc
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
targetos: Windows
req.typenames: D3D10_EFFECT_SHADER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_EFFECT_SHADER_DESC
 - d3d10effect/_D3D10_EFFECT_SHADER_DESC
 - D3D10_EFFECT_SHADER_DESC
 - d3d10effect/D3D10_EFFECT_SHADER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_EFFECT_SHADER_DESC
---

# D3D10_EFFECT_SHADER_DESC structure


## -description

Describes an effect shader.

## -struct-fields

### -field pInputSignature

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

Passed into CreateInputLayout. Only valid on a vertex shader or geometry shader. See <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createinputlayout">ID3D10Device_CreateInputLayout</a>.

### -field IsInline

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> is the shader is defined inline; otherwise <b>FALSE</b>.

### -field pBytecode

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

A pointer to the compiled shader.

### -field BytecodeLength

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The length of pBytecode.

### -field SODecl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that contains a declaration of the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">stream output </a> from a geometry shader.

### -field NumInputSignatureEntries

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of entries in the input signature.

### -field NumOutputSignatureEntries

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of entries in the output signature.

## -remarks

To get an effect-shader description, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectshadervariable-getshaderdesc">ID3D10EffectShaderVariable::GetShaderDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>