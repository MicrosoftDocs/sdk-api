---
UID: NS:d3d10effect._D3D10_EFFECT_DESC
title: D3D10_EFFECT_DESC (d3d10effect.h)
description: Describes an effect.
helpviewer_keywords: ["1f8c640b-441a-ed00-b882-58a32c647df9","D3D10_EFFECT_DESC","D3D10_EFFECT_DESC structure [Direct3D 10]","d3d10effect/D3D10_EFFECT_DESC","direct3d10.d3d10_effect_desc"]
old-location: direct3d10\d3d10_effect_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_effect_desc.htm
ms.date: 12/05/2018
ms.keywords: 1f8c640b-441a-ed00-b882-58a32c647df9, D3D10_EFFECT_DESC, D3D10_EFFECT_DESC structure [Direct3D 10], d3d10effect/D3D10_EFFECT_DESC, direct3d10.d3d10_effect_desc
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
req.typenames: D3D10_EFFECT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_EFFECT_DESC
 - d3d10effect/_D3D10_EFFECT_DESC
 - D3D10_EFFECT_DESC
 - d3d10effect/D3D10_EFFECT_DESC
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
 - D3D10_EFFECT_DESC
---

# D3D10_EFFECT_DESC structure


## -description

Describes an effect.

## -struct-fields

### -field IsChildEffect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the effect is a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects-performance">child effect</a>; otherwise <b>FALSE</b>.

### -field ConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of constant buffers.

### -field SharedConstantBuffers

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of constant buffers shared in an effect pool.

### -field GlobalVariables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of global variables.

### -field SharedGlobalVariables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of global variables shared in an effect pool.

### -field Techniques

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of techniques.

## -remarks

To get an effect description, call <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effect-getdesc">ID3D10Effect::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>