---
UID: NF:d3d10effect.ID3D10EffectRenderTargetViewVariable.GetRenderTargetArray
title: ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray (d3d10effect.h)
description: Get an array of render-targets.
helpviewer_keywords: ["55cfc9f6-d447-4ae4-5a22-e5d490eec17f","GetRenderTargetArray","GetRenderTargetArray method [Direct3D 10]","GetRenderTargetArray method [Direct3D 10]","ID3D10EffectRenderTargetViewVariable interface","ID3D10EffectRenderTargetViewVariable interface [Direct3D 10]","GetRenderTargetArray method","ID3D10EffectRenderTargetViewVariable.GetRenderTargetArray","ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray","d3d10effect/ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray","direct3d10.id3d10effectrendertargetviewvariable_getrendertargetarray"]
old-location: direct3d10\id3d10effectrendertargetviewvariable_getrendertargetarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrendertargetviewvariable_getrendertargetarray.htm
ms.date: 12/05/2018
ms.keywords: 55cfc9f6-d447-4ae4-5a22-e5d490eec17f, GetRenderTargetArray, GetRenderTargetArray method [Direct3D 10], GetRenderTargetArray method [Direct3D 10],ID3D10EffectRenderTargetViewVariable interface, ID3D10EffectRenderTargetViewVariable interface [Direct3D 10],GetRenderTargetArray method, ID3D10EffectRenderTargetViewVariable.GetRenderTargetArray, ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray, d3d10effect/ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray, direct3d10.id3d10effectrendertargetviewvariable_getrendertargetarray
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
 - ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray
 - d3d10effect/ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray
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
 - ID3D10EffectRenderTargetViewVariable.GetRenderTargetArray
---

# ID3D10EffectRenderTargetViewVariable::GetRenderTargetArray


## -description

Get an array of render-targets.

## -parameters

### -param ppResources [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>**</b>

A pointer to an array of render-target-view interfaces. See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView Interface</a>.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based array index to get the first interface.

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectrendertargetviewvariable">ID3D10EffectRenderTargetViewVariable Interface</a>