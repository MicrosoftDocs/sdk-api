---
UID: NS:d3d10effect._D3D10_PASS_DESC
title: D3D10_PASS_DESC (d3d10effect.h)
description: Describes an effect pass, which contains pipeline state.
helpviewer_keywords: ["5373c44b-9837-094e-9520-1b3a2078a9d6","D3D10_PASS_DESC","D3D10_PASS_DESC structure [Direct3D 10]","d3d10effect/D3D10_PASS_DESC","direct3d10.d3d10_pass_desc"]
old-location: direct3d10\d3d10_pass_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_pass_desc.htm
ms.date: 12/05/2018
ms.keywords: 5373c44b-9837-094e-9520-1b3a2078a9d6, D3D10_PASS_DESC, D3D10_PASS_DESC structure [Direct3D 10], d3d10effect/D3D10_PASS_DESC, direct3d10.d3d10_pass_desc
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
req.typenames: D3D10_PASS_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_PASS_DESC
 - d3d10effect/_D3D10_PASS_DESC
 - D3D10_PASS_DESC
 - d3d10effect/D3D10_PASS_DESC
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
 - D3D10_PASS_DESC
---

# D3D10_PASS_DESC structure


## -description

Describes an effect pass, which contains pipeline state.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

A string that contains the name of the pass; otherwise <b>NULL</b>.

### -field Annotations

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of annotations.

### -field pIAInputSignature

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

A pointer to the input signature or the vertex shader; otherwise <b>NULL</b>.

### -field IAInputSignatureSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size of the input signature (in bytes).

### -field StencilRef

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The stencil-reference value used in the depth-stencil state (see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-depth-stencil">Configuring Depth-Stencil Functionality (Direct3D 10)</a>).

### -field SampleMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The sample mask for the blend state (see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">Configuring Blending Functionality (Direct3D 10)</a>).

### -field BlendFactor

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The per-component blend factors (RGBA) for the blend state (see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">Configuring Blending Functionality (Direct3D 10)</a>).

## -remarks

Get a pass description by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getdesc">ID3D10EffectPass::GetDesc</a>; an effect technique contains one or more passes.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>