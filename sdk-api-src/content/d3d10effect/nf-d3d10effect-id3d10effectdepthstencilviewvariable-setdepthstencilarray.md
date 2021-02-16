---
UID: NF:d3d10effect.ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray
title: ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray (d3d10effect.h)
description: Set an array of depth-stencil-view resources.
helpviewer_keywords: ["19d677a4-86e6-d451-5d65-7ab228f247d5","ID3D10EffectDepthStencilViewVariable interface [Direct3D 10]","SetDepthStencilArray method","ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray","ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray","SetDepthStencilArray","SetDepthStencilArray method [Direct3D 10]","SetDepthStencilArray method [Direct3D 10]","ID3D10EffectDepthStencilViewVariable interface","d3d10effect/ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray","direct3d10.id3d10effectdepthstencilviewvariable_setdepthstencilarray"]
old-location: direct3d10\id3d10effectdepthstencilviewvariable_setdepthstencilarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectdepthstencilviewvariable_setdepthstencilarray.htm
ms.date: 12/05/2018
ms.keywords: 19d677a4-86e6-d451-5d65-7ab228f247d5, ID3D10EffectDepthStencilViewVariable interface [Direct3D 10],SetDepthStencilArray method, ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray, ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray, SetDepthStencilArray, SetDepthStencilArray method [Direct3D 10], SetDepthStencilArray method [Direct3D 10],ID3D10EffectDepthStencilViewVariable interface, d3d10effect/ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray, direct3d10.id3d10effectdepthstencilviewvariable_setdepthstencilarray
req.header: d3d10effect.h
req.include-header: D3d10
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
 - ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray
 - d3d10effect/ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d10effect.h
api_name:
 - ID3D10EffectDepthStencilViewVariable.SetDepthStencilArray
---

# ID3D10EffectDepthStencilViewVariable::SetDepthStencilArray


## -description

Set an array of depth-stencil-view resources.

## -parameters

### -param ppResources [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>**</b>

A pointer to an array of depth-stencil-view interfaces. See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView Interface</a>.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based array index to set the first interface.

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable">ID3D10EffectDepthStencilViewVariable Interface</a>