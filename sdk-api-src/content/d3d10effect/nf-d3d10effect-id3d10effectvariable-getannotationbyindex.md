---
UID: NF:d3d10effect.ID3D10EffectVariable.GetAnnotationByIndex
title: ID3D10EffectVariable::GetAnnotationByIndex (d3d10effect.h)
description: The ID3D10EffectVariable::GetAnnotationByIndex (d3d10effect.h) method gets an annotation by index.
helpviewer_keywords: ["GetAnnotationByIndex","GetAnnotationByIndex method [Direct3D 10]","GetAnnotationByIndex method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetAnnotationByIndex method","ID3D10EffectVariable.GetAnnotationByIndex","ID3D10EffectVariable::GetAnnotationByIndex","c60bf6b1-5d05-ec0d-545c-b26e3e436ab8","d3d10effect/ID3D10EffectVariable::GetAnnotationByIndex","direct3d10.id3d10effectvariable_getannotationbyindex"]
old-location: direct3d10\id3d10effectvariable_getannotationbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getannotationbyindex.htm
ms.date: 08/10/2022
ms.keywords: GetAnnotationByIndex, GetAnnotationByIndex method [Direct3D 10], GetAnnotationByIndex method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetAnnotationByIndex method, ID3D10EffectVariable.GetAnnotationByIndex, ID3D10EffectVariable::GetAnnotationByIndex, c60bf6b1-5d05-ec0d-545c-b26e3e436ab8, d3d10effect/ID3D10EffectVariable::GetAnnotationByIndex, direct3d10.id3d10effectvariable_getannotationbyindex
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
 - ID3D10EffectVariable::GetAnnotationByIndex
 - d3d10effect/ID3D10EffectVariable::GetAnnotationByIndex
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
 - ID3D10EffectVariable.GetAnnotationByIndex
---

# ID3D10EffectVariable::GetAnnotationByIndex


## -description

Get an annotation by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

Annotations can be attached to a technique, a pass or a global variable. For the syntax, see <a href="/windows/desktop/direct3d10/d3d10-effect-annotation-syntax">Annotation Syntax (Direct3D 10)</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>