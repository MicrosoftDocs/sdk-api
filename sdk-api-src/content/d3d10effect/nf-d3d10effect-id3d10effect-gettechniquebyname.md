---
UID: NF:d3d10effect.ID3D10Effect.GetTechniqueByName
title: ID3D10Effect::GetTechniqueByName (d3d10effect.h)
description: Get a technique by name.
helpviewer_keywords: ["85db30ea-1e49-0b62-caca-5e0cf8959361","GetTechniqueByName","GetTechniqueByName method [Direct3D 10]","GetTechniqueByName method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetTechniqueByName method","ID3D10Effect.GetTechniqueByName","ID3D10Effect::GetTechniqueByName","d3d10effect/ID3D10Effect::GetTechniqueByName","direct3d10.id3d10effect_gettechniquebyname"]
old-location: direct3d10\id3d10effect_gettechniquebyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_gettechniquebyname.htm
ms.date: 12/05/2018
ms.keywords: 85db30ea-1e49-0b62-caca-5e0cf8959361, GetTechniqueByName, GetTechniqueByName method [Direct3D 10], GetTechniqueByName method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetTechniqueByName method, ID3D10Effect.GetTechniqueByName, ID3D10Effect::GetTechniqueByName, d3d10effect/ID3D10Effect::GetTechniqueByName, direct3d10.id3d10effect_gettechniquebyname
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
 - ID3D10Effect::GetTechniqueByName
 - d3d10effect/ID3D10Effect::GetTechniqueByName
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
 - ID3D10Effect.GetTechniqueByName
---

# ID3D10Effect::GetTechniqueByName


## -description

Get a technique by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the technique.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique Interface</a>, or <b>NULL</b> if the technique is not found.

## -remarks

An effect contains one or more techniques; each technique contains one or more passes. You can access a technique using its name or with an index. For more about techniques, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-organize">techniques and passes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>