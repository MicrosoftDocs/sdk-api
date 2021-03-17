---
UID: NF:d3d10effect.ID3D10EffectVariable.GetElement
title: ID3D10EffectVariable::GetElement (d3d10effect.h)
description: Get an array element.
helpviewer_keywords: ["9b0e159b-0d15-0249-35fe-c610c699f1ba","GetElement","GetElement method [Direct3D 10]","GetElement method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetElement method","ID3D10EffectVariable.GetElement","ID3D10EffectVariable::GetElement","d3d10effect/ID3D10EffectVariable::GetElement","direct3d10.id3d10effectvariable_getelement"]
old-location: direct3d10\id3d10effectvariable_getelement.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getelement.htm
ms.date: 12/05/2018
ms.keywords: 9b0e159b-0d15-0249-35fe-c610c699f1ba, GetElement, GetElement method [Direct3D 10], GetElement method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetElement method, ID3D10EffectVariable.GetElement, ID3D10EffectVariable::GetElement, d3d10effect/ID3D10EffectVariable::GetElement, direct3d10.id3d10effectvariable_getelement
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
 - ID3D10EffectVariable::GetElement
 - d3d10effect/ID3D10EffectVariable::GetElement
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
 - ID3D10EffectVariable.GetElement
---

# ID3D10EffectVariable::GetElement


## -description

Get an array element.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index; otherwise 0.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

If the effect variable is an array, use this method to return one of the elements.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>