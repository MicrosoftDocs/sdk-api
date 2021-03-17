---
UID: NS:d3d10effect._D3D10_TECHNIQUE_DESC
title: D3D10_TECHNIQUE_DESC (d3d10effect.h)
description: Describes an effect technique.
helpviewer_keywords: ["506d7648-e159-3365-396e-418be67bb2d9","D3D10_TECHNIQUE_DESC","D3D10_TECHNIQUE_DESC structure [Direct3D 10]","d3d10effect/D3D10_TECHNIQUE_DESC","direct3d10.d3d10_technique_desc"]
old-location: direct3d10\d3d10_technique_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_technique_desc.htm
ms.date: 12/05/2018
ms.keywords: 506d7648-e159-3365-396e-418be67bb2d9, D3D10_TECHNIQUE_DESC, D3D10_TECHNIQUE_DESC structure [Direct3D 10], d3d10effect/D3D10_TECHNIQUE_DESC, direct3d10.d3d10_technique_desc
req.header: d3d10effect.h
req.include-header: D3D10.h
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
req.typenames: D3D10_TECHNIQUE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_TECHNIQUE_DESC
 - d3d10effect/_D3D10_TECHNIQUE_DESC
 - D3D10_TECHNIQUE_DESC
 - d3d10effect/D3D10_TECHNIQUE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_TECHNIQUE_DESC
---

# D3D10_TECHNIQUE_DESC structure


## -description

Describes an effect technique.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that contains the technique name; otherwise <b>NULL</b>.

### -field Passes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of passes in the technique.

### -field Annotations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of annotations.

## -remarks

To get a technique, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-getdesc">ID3D10EffectTechnique::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>