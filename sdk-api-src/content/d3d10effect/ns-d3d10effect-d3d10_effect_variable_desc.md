---
UID: NS:d3d10effect._D3D10_EFFECT_VARIABLE_DESC
title: D3D10_EFFECT_VARIABLE_DESC (d3d10effect.h)
description: Describes an effect variable.
helpviewer_keywords: ["D3D10_EFFECT_VARIABLE_DESC","D3D10_EFFECT_VARIABLE_DESC structure [Direct3D 10]","d3d10effect/D3D10_EFFECT_VARIABLE_DESC","direct3d10.d3d10_effect_variable_desc","e24d998a-d966-5f94-eabb-5d6535c0928a"]
old-location: direct3d10\d3d10_effect_variable_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_variable_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_EFFECT_VARIABLE_DESC, D3D10_EFFECT_VARIABLE_DESC structure [Direct3D 10], d3d10effect/D3D10_EFFECT_VARIABLE_DESC, direct3d10.d3d10_effect_variable_desc, e24d998a-d966-5f94-eabb-5d6535c0928a
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
req.typenames: D3D10_EFFECT_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_EFFECT_VARIABLE_DESC
 - d3d10effect/_D3D10_EFFECT_VARIABLE_DESC
 - D3D10_EFFECT_VARIABLE_DESC
 - d3d10effect/D3D10_EFFECT_VARIABLE_DESC
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
 - D3D10_EFFECT_VARIABLE_DESC
---

# D3D10_EFFECT_VARIABLE_DESC structure


## -description

Describes an effect variable.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that contains the variable name.

### -field Semantic

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The semantic attached to the variable; otherwise <b>NULL</b>.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants">flags</a> for effect variables.

### -field Annotations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of annotations; otherwise 0.

### -field BufferOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset between the beginning of the constant buffer and this variable; otherwise 0.

### -field ExplicitBindPoint

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The register that this variable is bound to. To bind a variable explicitly use the D3D10_EFFECT_VARIABLE_EXPLICIT_BIND_POINT flag.

## -remarks

To get an effect-variable description, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-getdesc">ID3D10EffectVariable::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>