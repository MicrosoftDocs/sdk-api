---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetShaderDesc
title: ID3D10EffectShaderVariable::GetShaderDesc (d3d10effect.h)
author: windows-sdk-content
description: Get a shader description.
old-location: direct3d10\id3d10effectshadervariable_getshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getshaderdesc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetShaderDesc, GetShaderDesc method [Direct3D 10], GetShaderDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetShaderDesc method, ID3D10EffectShaderVariable.GetShaderDesc, ID3D10EffectShaderVariable::GetShaderDesc, d3d10effect/ID3D10EffectShaderVariable::GetShaderDesc, direct3d10.id3d10effectshadervariable_getshaderdesc, eb630246-c382-1984-9a6c-712450dfdd06
ms.topic: method
f1_keywords:
- d3d10effect/ID3D10EffectShaderVariable.GetShaderDesc
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10Effect.h
api_name:
- ID3D10EffectShaderVariable.GetShaderDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectShaderVariable::GetShaderDesc


## -description


Get a shader description.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.


### -param pDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_effect_shader_desc">D3D10_EFFECT_SHADER_DESC</a>*</b>

A pointer to a shader description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_effect_shader_desc">D3D10_EFFECT_SHADER_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>
 

 

