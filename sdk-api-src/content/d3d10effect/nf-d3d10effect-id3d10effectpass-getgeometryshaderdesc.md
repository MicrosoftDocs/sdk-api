---
UID: NF:d3d10effect.ID3D10EffectPass.GetGeometryShaderDesc
title: ID3D10EffectPass::GetGeometryShaderDesc (d3d10effect.h)
description: Get a geometry-shader description.
helpviewer_keywords: ["1f200fc8-f573-7b6c-75f4-5b7cf7a95eb1","GetGeometryShaderDesc","GetGeometryShaderDesc method [Direct3D 10]","GetGeometryShaderDesc method [Direct3D 10]","ID3D10EffectPass interface","ID3D10EffectPass interface [Direct3D 10]","GetGeometryShaderDesc method","ID3D10EffectPass.GetGeometryShaderDesc","ID3D10EffectPass::GetGeometryShaderDesc","d3d10effect/ID3D10EffectPass::GetGeometryShaderDesc","direct3d10.id3d10effectpass_getgeometryshaderdesc"]
old-location: direct3d10\id3d10effectpass_getgeometryshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getgeometryshaderdesc.htm
ms.date: 12/05/2018
ms.keywords: 1f200fc8-f573-7b6c-75f4-5b7cf7a95eb1, GetGeometryShaderDesc, GetGeometryShaderDesc method [Direct3D 10], GetGeometryShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetGeometryShaderDesc method, ID3D10EffectPass.GetGeometryShaderDesc, ID3D10EffectPass::GetGeometryShaderDesc, d3d10effect/ID3D10EffectPass::GetGeometryShaderDesc, direct3d10.id3d10effectpass_getgeometryshaderdesc
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
 - ID3D10EffectPass::GetGeometryShaderDesc
 - d3d10effect/ID3D10EffectPass::GetGeometryShaderDesc
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
 - ID3D10EffectPass.GetGeometryShaderDesc
---

# ID3D10EffectPass::GetGeometryShaderDesc


## -description

Get a geometry-shader description.

## -parameters

### -param pDesc [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a geometry-shader description (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect pass can contain render state assignments and shader object assignments.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>