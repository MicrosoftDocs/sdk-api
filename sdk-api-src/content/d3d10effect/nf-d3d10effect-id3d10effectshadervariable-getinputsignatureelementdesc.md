---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetInputSignatureElementDesc
title: ID3D10EffectShaderVariable::GetInputSignatureElementDesc (d3d10effect.h)
description: Get an input-signature description.
helpviewer_keywords: ["22632913-ab5d-3124-504e-d04b7e203897","GetInputSignatureElementDesc","GetInputSignatureElementDesc method [Direct3D 10]","GetInputSignatureElementDesc method [Direct3D 10]","ID3D10EffectShaderVariable interface","ID3D10EffectShaderVariable interface [Direct3D 10]","GetInputSignatureElementDesc method","ID3D10EffectShaderVariable.GetInputSignatureElementDesc","ID3D10EffectShaderVariable::GetInputSignatureElementDesc","d3d10effect/ID3D10EffectShaderVariable::GetInputSignatureElementDesc","direct3d10.id3d10effectshadervariable_getinputsignatureelementdesc"]
old-location: direct3d10\id3d10effectshadervariable_getinputsignatureelementdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getinputsignatureelementdesc.htm
ms.date: 12/05/2018
ms.keywords: 22632913-ab5d-3124-504e-d04b7e203897, GetInputSignatureElementDesc, GetInputSignatureElementDesc method [Direct3D 10], GetInputSignatureElementDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetInputSignatureElementDesc method, ID3D10EffectShaderVariable.GetInputSignatureElementDesc, ID3D10EffectShaderVariable::GetInputSignatureElementDesc, d3d10effect/ID3D10EffectShaderVariable::GetInputSignatureElementDesc, direct3d10.id3d10effectshadervariable_getinputsignatureelementdesc
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
 - ID3D10EffectShaderVariable::GetInputSignatureElementDesc
 - d3d10effect/ID3D10EffectShaderVariable::GetInputSignatureElementDesc
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
 - ID3D10EffectShaderVariable.GetInputSignatureElementDesc
---

# ID3D10EffectShaderVariable::GetInputSignatureElementDesc


## -description

Get an input-signature description.

## -parameters

### -param ShaderIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based shader index.

### -param Element [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based shader-element index.

### -param pDesc [in]

Type: <b><a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a parameter description (see <a href="/windows/win32/api/d3d10shader/ns-d3d10shader-d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters). The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>