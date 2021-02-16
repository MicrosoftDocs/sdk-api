---
UID: NF:d3d10effect.ID3D10Effect.GetVariableBySemantic
title: ID3D10Effect::GetVariableBySemantic (d3d10effect.h)
description: Get a variable by semantic.
helpviewer_keywords: ["GetVariableBySemantic","GetVariableBySemantic method [Direct3D 10]","GetVariableBySemantic method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetVariableBySemantic method","ID3D10Effect.GetVariableBySemantic","ID3D10Effect::GetVariableBySemantic","d3d10effect/ID3D10Effect::GetVariableBySemantic","direct3d10.id3d10effect_getvariablebysemantic","e578cd0d-594a-b43e-8baa-310f0b747079"]
old-location: direct3d10\id3d10effect_getvariablebysemantic.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebysemantic.htm
ms.date: 12/05/2018
ms.keywords: GetVariableBySemantic, GetVariableBySemantic method [Direct3D 10], GetVariableBySemantic method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableBySemantic method, ID3D10Effect.GetVariableBySemantic, ID3D10Effect::GetVariableBySemantic, d3d10effect/ID3D10Effect::GetVariableBySemantic, direct3d10.id3d10effect_getvariablebysemantic, e578cd0d-594a-b43e-8baa-310f0b747079
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
 - ID3D10Effect::GetVariableBySemantic
 - d3d10effect/ID3D10Effect::GetVariableBySemantic
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
 - ID3D10Effect.GetVariableBySemantic
---

# ID3D10Effect::GetVariableBySemantic


## -description

Get a variable by semantic.

## -parameters

### -param Semantic [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The semantic name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to the effect variable indicated by the Semantic. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

Each effect variable can have a semantic attached, which is a user defined metadata string. Some <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">system-value semantics</a> are reserved words that trigger built in functionality by pipeline stages.

The method returns a pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">effect-variable interface</a> if a variable is not found; you can call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-isvalid">ID3D10Effect::IsValid</a> to verify whether or not the semantic exists.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>