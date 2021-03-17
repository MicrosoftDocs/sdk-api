---
UID: NF:d3d10effect.ID3D10EffectPass.GetPixelShaderDesc
title: ID3D10EffectPass::GetPixelShaderDesc (d3d10effect.h)
description: Get a pixel-shader description.
helpviewer_keywords: ["GetPixelShaderDesc","GetPixelShaderDesc method [Direct3D 10]","GetPixelShaderDesc method [Direct3D 10]","ID3D10EffectPass interface","ID3D10EffectPass interface [Direct3D 10]","GetPixelShaderDesc method","ID3D10EffectPass.GetPixelShaderDesc","ID3D10EffectPass::GetPixelShaderDesc","d3d10effect/ID3D10EffectPass::GetPixelShaderDesc","direct3d10.id3d10effectpass_getpixelshaderdesc","e9a087a4-34ef-3b9b-ee16-34ff7080b051"]
old-location: direct3d10\id3d10effectpass_getpixelshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getpixelshaderdesc.htm
ms.date: 12/05/2018
ms.keywords: GetPixelShaderDesc, GetPixelShaderDesc method [Direct3D 10], GetPixelShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetPixelShaderDesc method, ID3D10EffectPass.GetPixelShaderDesc, ID3D10EffectPass::GetPixelShaderDesc, d3d10effect/ID3D10EffectPass::GetPixelShaderDesc, direct3d10.id3d10effectpass_getpixelshaderdesc, e9a087a4-34ef-3b9b-ee16-34ff7080b051
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
 - ID3D10EffectPass::GetPixelShaderDesc
 - d3d10effect/ID3D10EffectPass::GetPixelShaderDesc
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
 - ID3D10EffectPass.GetPixelShaderDesc
---

# ID3D10EffectPass::GetPixelShaderDesc


## -description

Get a pixel-shader description.

## -parameters

### -param pDesc [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a pixel-shader description (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect pass can contain render state assignments and shader object assignments.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>