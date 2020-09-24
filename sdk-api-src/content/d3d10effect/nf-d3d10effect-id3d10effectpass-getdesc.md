---
UID: NF:d3d10effect.ID3D10EffectPass.GetDesc
title: ID3D10EffectPass::GetDesc (d3d10effect.h)
description: Get a pass description.
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 10]","GetDesc method [Direct3D 10]","ID3D10EffectPass interface","ID3D10EffectPass interface [Direct3D 10]","GetDesc method","ID3D10EffectPass.GetDesc","ID3D10EffectPass::GetDesc","d144db62-661e-4008-27bf-01ee2d40f810","d3d10effect/ID3D10EffectPass::GetDesc","direct3d10.id3d10effectpass_getdesc"]
old-location: direct3d10\id3d10effectpass_getdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getdesc.htm
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetDesc method, ID3D10EffectPass.GetDesc, ID3D10EffectPass::GetDesc, d144db62-661e-4008-27bf-01ee2d40f810, d3d10effect/ID3D10EffectPass::GetDesc, direct3d10.id3d10effectpass_getdesc
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
 - ID3D10EffectPass::GetDesc
 - d3d10effect/ID3D10EffectPass::GetDesc
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
 - ID3D10EffectPass.GetDesc
---

# ID3D10EffectPass::GetDesc


## -description

Get a pass description.

## -parameters

### -param pDesc [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc">D3D10_PASS_DESC</a>*</b>

A pointer to a pass description (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc">D3D10_PASS_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures). An effect technique contains one or more passes. See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-organize">techniques and passes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>