---
UID: NF:d3d10effect.ID3D10EffectTechnique.GetAnnotationByName
title: ID3D10EffectTechnique::GetAnnotationByName (d3d10effect.h)
description: Get an annotation by name. (ID3D10EffectTechnique.GetAnnotationByName)
helpviewer_keywords: ["GetAnnotationByName","GetAnnotationByName method [Direct3D 10]","GetAnnotationByName method [Direct3D 10]","ID3D10EffectTechnique interface","ID3D10EffectTechnique interface [Direct3D 10]","GetAnnotationByName method","ID3D10EffectTechnique.GetAnnotationByName","ID3D10EffectTechnique::GetAnnotationByName","bab9e1c3-3845-0dbe-c407-02592ee3101c","d3d10effect/ID3D10EffectTechnique::GetAnnotationByName","direct3d10.id3d10effecttechnique_getannotationbyname"]
old-location: direct3d10\id3d10effecttechnique_getannotationbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_getannotationbyname.htm
ms.date: 12/05/2018
ms.keywords: GetAnnotationByName, GetAnnotationByName method [Direct3D 10], GetAnnotationByName method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],GetAnnotationByName method, ID3D10EffectTechnique.GetAnnotationByName, ID3D10EffectTechnique::GetAnnotationByName, bab9e1c3-3845-0dbe-c407-02592ee3101c, d3d10effect/ID3D10EffectTechnique::GetAnnotationByName, direct3d10.id3d10effecttechnique_getannotationbyname
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
 - ID3D10EffectTechnique::GetAnnotationByName
 - d3d10effect/ID3D10EffectTechnique::GetAnnotationByName
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
 - ID3D10EffectTechnique.GetAnnotationByName
---

# ID3D10EffectTechnique::GetAnnotationByName


## -description

Get an annotation by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Name of the annotation.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

Use an annotation to attach a piece of metadata to a technique.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique Interface</a>
