---
UID: NF:d3d10effect.ID3D10EffectVariable.GetAnnotationByName
title: ID3D10EffectVariable::GetAnnotationByName (d3d10effect.h)
description: Get an annotation by name. (ID3D10EffectVariable.GetAnnotationByName)
helpviewer_keywords: ["88e41418-934c-2f28-baec-b4fa95311890","GetAnnotationByName","GetAnnotationByName method [Direct3D 10]","GetAnnotationByName method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetAnnotationByName method","ID3D10EffectVariable.GetAnnotationByName","ID3D10EffectVariable::GetAnnotationByName","d3d10effect/ID3D10EffectVariable::GetAnnotationByName","direct3d10.id3d10effectvariable_getannotationbyname"]
old-location: direct3d10\id3d10effectvariable_getannotationbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getannotationbyname.htm
ms.date: 12/05/2018
ms.keywords: 88e41418-934c-2f28-baec-b4fa95311890, GetAnnotationByName, GetAnnotationByName method [Direct3D 10], GetAnnotationByName method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetAnnotationByName method, ID3D10EffectVariable.GetAnnotationByName, ID3D10EffectVariable::GetAnnotationByName, d3d10effect/ID3D10EffectVariable::GetAnnotationByName, direct3d10.id3d10effectvariable_getannotationbyname
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
 - ID3D10EffectVariable::GetAnnotationByName
 - d3d10effect/ID3D10EffectVariable::GetAnnotationByName
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
 - ID3D10EffectVariable.GetAnnotationByName
---

# ID3D10EffectVariable::GetAnnotationByName


## -description

Get an annotation by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The annotation name.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.  Note that if the annotation is not found the <b>ID3D10EffectVariable Interface</b> returned will be empty. The <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">ID3D10EffectVariable::IsValid</a> method should be called to determine whether the annotation was found.

## -remarks

Annotations can be attached to a technique, a pass or a global variable. For the syntax, see <a href="/windows/desktop/direct3d10/d3d10-effect-annotation-syntax">Annotation Syntax (Direct3D 10)</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
