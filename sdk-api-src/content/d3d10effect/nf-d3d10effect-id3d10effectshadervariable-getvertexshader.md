---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetVertexShader
title: ID3D10EffectShaderVariable::GetVertexShader (d3d10effect.h)
description: Get a vertex shader.
helpviewer_keywords: ["GetVertexShader","GetVertexShader method [Direct3D 10]","GetVertexShader method [Direct3D 10]","ID3D10EffectShaderVariable interface","ID3D10EffectShaderVariable interface [Direct3D 10]","GetVertexShader method","ID3D10EffectShaderVariable.GetVertexShader","ID3D10EffectShaderVariable::GetVertexShader","d3d10effect/ID3D10EffectShaderVariable::GetVertexShader","d42282c4-3590-3201-8fd7-e13e4054fb34","direct3d10.id3d10effectshadervariable_getvertexshader"]
old-location: direct3d10\id3d10effectshadervariable_getvertexshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getvertexshader.htm
ms.date: 12/05/2018
ms.keywords: GetVertexShader, GetVertexShader method [Direct3D 10], GetVertexShader method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetVertexShader method, ID3D10EffectShaderVariable.GetVertexShader, ID3D10EffectShaderVariable::GetVertexShader, d3d10effect/ID3D10EffectShaderVariable::GetVertexShader, d42282c4-3590-3201-8fd7-e13e4054fb34, direct3d10.id3d10effectshadervariable_getvertexshader
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
 - ID3D10EffectShaderVariable::GetVertexShader
 - d3d10effect/ID3D10EffectShaderVariable::GetVertexShader
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
 - ID3D10EffectShaderVariable.GetVertexShader
---

# ID3D10EffectShaderVariable::GetVertexShader


## -description

Get a vertex shader.

## -parameters

### -param ShaderIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.

### -param ppVS [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader</a>**</b>

A pointer to a <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>