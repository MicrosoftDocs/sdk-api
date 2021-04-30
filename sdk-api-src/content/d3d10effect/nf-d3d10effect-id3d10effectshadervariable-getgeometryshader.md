---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetGeometryShader
title: ID3D10EffectShaderVariable::GetGeometryShader (d3d10effect.h)
description: Get a geometry shader.
helpviewer_keywords: ["3ec86a63-120a-f1df-c229-bbdd165c6650","GetGeometryShader","GetGeometryShader method [Direct3D 10]","GetGeometryShader method [Direct3D 10]","ID3D10EffectShaderVariable interface","ID3D10EffectShaderVariable interface [Direct3D 10]","GetGeometryShader method","ID3D10EffectShaderVariable.GetGeometryShader","ID3D10EffectShaderVariable::GetGeometryShader","d3d10effect/ID3D10EffectShaderVariable::GetGeometryShader","direct3d10.id3d10effectshadervariable_getgeometryshader"]
old-location: direct3d10\id3d10effectshadervariable_getgeometryshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getgeometryshader.htm
ms.date: 12/05/2018
ms.keywords: 3ec86a63-120a-f1df-c229-bbdd165c6650, GetGeometryShader, GetGeometryShader method [Direct3D 10], GetGeometryShader method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetGeometryShader method, ID3D10EffectShaderVariable.GetGeometryShader, ID3D10EffectShaderVariable::GetGeometryShader, d3d10effect/ID3D10EffectShaderVariable::GetGeometryShader, direct3d10.id3d10effectshadervariable_getgeometryshader
req.header: d3d10effect.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectShaderVariable::GetGeometryShader
 - d3d10effect/ID3D10EffectShaderVariable::GetGeometryShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectShaderVariable.GetGeometryShader
---

# ID3D10EffectShaderVariable::GetGeometryShader


## -description

Get a geometry shader.

## -parameters

### -param ShaderIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.

### -param ppGS [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader</a>**</b>

A pointer to a <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>