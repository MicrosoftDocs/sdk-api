---
UID: NF:d3d10effect.ID3D10EffectTechnique.GetAnnotationByIndex
title: ID3D10EffectTechnique::GetAnnotationByIndex (d3d10effect.h)
description: The ID3D10EffectTechnique::GetAnnotationByIndex (d3d10effect.h) method gets an annotation by index.
helpviewer_keywords: ["03441718-a147-0c52-e3f6-b191b7f1fa7d","GetAnnotationByIndex","GetAnnotationByIndex method [Direct3D 10]","GetAnnotationByIndex method [Direct3D 10]","ID3D10EffectTechnique interface","ID3D10EffectTechnique interface [Direct3D 10]","GetAnnotationByIndex method","ID3D10EffectTechnique.GetAnnotationByIndex","ID3D10EffectTechnique::GetAnnotationByIndex","d3d10effect/ID3D10EffectTechnique::GetAnnotationByIndex","direct3d10.id3d10effecttechnique_getannotationbyindex"]
old-location: direct3d10\id3d10effecttechnique_getannotationbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_getannotationbyindex.htm
ms.date: 08/10/2022
ms.keywords: 03441718-a147-0c52-e3f6-b191b7f1fa7d, GetAnnotationByIndex, GetAnnotationByIndex method [Direct3D 10], GetAnnotationByIndex method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],GetAnnotationByIndex method, ID3D10EffectTechnique.GetAnnotationByIndex, ID3D10EffectTechnique::GetAnnotationByIndex, d3d10effect/ID3D10EffectTechnique::GetAnnotationByIndex, direct3d10.id3d10effecttechnique_getannotationbyindex
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
 - ID3D10EffectTechnique::GetAnnotationByIndex
 - d3d10effect/ID3D10EffectTechnique::GetAnnotationByIndex
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
 - ID3D10EffectTechnique.GetAnnotationByIndex
---

# ID3D10EffectTechnique::GetAnnotationByIndex


## -description

Get an annotation by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the interface pointer.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

Use an annotation to attach a piece of metadata to a technique.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique Interface</a>