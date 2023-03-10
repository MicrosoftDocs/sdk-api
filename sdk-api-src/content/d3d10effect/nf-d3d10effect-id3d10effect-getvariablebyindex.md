---
UID: NF:d3d10effect.ID3D10Effect.GetVariableByIndex
title: ID3D10Effect::GetVariableByIndex (d3d10effect.h)
description: Get a variable by index.
helpviewer_keywords: ["2e86399d-6be5-f4d4-507f-83c86d62cf4d","GetVariableByIndex","GetVariableByIndex method [Direct3D 10]","GetVariableByIndex method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetVariableByIndex method","ID3D10Effect.GetVariableByIndex","ID3D10Effect::GetVariableByIndex","d3d10effect/ID3D10Effect::GetVariableByIndex","direct3d10.id3d10effect_getvariablebyindex"]
old-location: direct3d10\id3d10effect_getvariablebyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebyindex.htm
ms.date: 12/05/2018
ms.keywords: 2e86399d-6be5-f4d4-507f-83c86d62cf4d, GetVariableByIndex, GetVariableByIndex method [Direct3D 10], GetVariableByIndex method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableByIndex method, ID3D10Effect.GetVariableByIndex, ID3D10Effect::GetVariableByIndex, d3d10effect/ID3D10Effect::GetVariableByIndex, direct3d10.id3d10effect_getvariablebyindex
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
 - ID3D10Effect::GetVariableByIndex
 - d3d10effect/ID3D10Effect::GetVariableByIndex
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
 - ID3D10Effect.GetVariableByIndex
---

# ID3D10Effect::GetVariableByIndex


## -description

Get a variable by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

An effect may contain one or more variables. Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique. You can access any local non-static effect variable using its name or with an index.

The method returns a pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">effect-variable interface</a> if a variable is not found; you can call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-isvalid">ID3D10Effect::IsValid</a> to verify whether or not the index exists.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>