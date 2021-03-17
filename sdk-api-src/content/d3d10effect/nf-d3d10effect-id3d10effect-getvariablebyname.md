---
UID: NF:d3d10effect.ID3D10Effect.GetVariableByName
title: ID3D10Effect::GetVariableByName (d3d10effect.h)
description: Get a variable by name.
helpviewer_keywords: ["GetVariableByName","GetVariableByName method [Direct3D 10]","GetVariableByName method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetVariableByName method","ID3D10Effect.GetVariableByName","ID3D10Effect::GetVariableByName","c08eacd5-3abc-89d5-a465-058f2f195794","d3d10effect/ID3D10Effect::GetVariableByName","direct3d10.id3d10effect_getvariablebyname"]
old-location: direct3d10\id3d10effect_getvariablebyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebyname.htm
ms.date: 12/05/2018
ms.keywords: GetVariableByName, GetVariableByName method [Direct3D 10], GetVariableByName method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableByName method, ID3D10Effect.GetVariableByName, ID3D10Effect::GetVariableByName, c08eacd5-3abc-89d5-a465-058f2f195794, d3d10effect/ID3D10Effect::GetVariableByName, direct3d10.id3d10effect_getvariablebyname
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
 - ID3D10Effect::GetVariableByName
 - d3d10effect/ID3D10Effect::GetVariableByName
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
 - ID3D10Effect.GetVariableByName
---

# ID3D10Effect::GetVariableByName


## -description

Get a variable by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The variable name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

An effect may contain one or more variables. Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique. You can access an effect variable using its name or with an index.

The method returns a pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">effect-variable interface</a> if a variable is not found; you can call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-isvalid">ID3D10Effect::IsValid</a> to verify whether or not the name exists.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>