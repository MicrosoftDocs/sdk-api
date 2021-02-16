---
UID: NF:d3d10effect.ID3D10EffectShaderResourceVariable.GetResourceArray
title: ID3D10EffectShaderResourceVariable::GetResourceArray (d3d10effect.h)
description: Get an array of shader resources.
helpviewer_keywords: ["GetResourceArray","GetResourceArray method [Direct3D 10]","GetResourceArray method [Direct3D 10]","ID3D10EffectShaderResourceVariable interface","ID3D10EffectShaderResourceVariable interface [Direct3D 10]","GetResourceArray method","ID3D10EffectShaderResourceVariable.GetResourceArray","ID3D10EffectShaderResourceVariable::GetResourceArray","be202163-a9e9-5354-d781-12b5b98cda4b","d3d10effect/ID3D10EffectShaderResourceVariable::GetResourceArray","direct3d10.id3d10effectshaderresourcevariable_getresourcearray"]
old-location: direct3d10\id3d10effectshaderresourcevariable_getresourcearray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshaderresourcevariable_getresourcearray.htm
ms.date: 12/05/2018
ms.keywords: GetResourceArray, GetResourceArray method [Direct3D 10], GetResourceArray method [Direct3D 10],ID3D10EffectShaderResourceVariable interface, ID3D10EffectShaderResourceVariable interface [Direct3D 10],GetResourceArray method, ID3D10EffectShaderResourceVariable.GetResourceArray, ID3D10EffectShaderResourceVariable::GetResourceArray, be202163-a9e9-5354-d781-12b5b98cda4b, d3d10effect/ID3D10EffectShaderResourceVariable::GetResourceArray, direct3d10.id3d10effectshaderresourcevariable_getresourcearray
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
 - ID3D10EffectShaderResourceVariable::GetResourceArray
 - d3d10effect/ID3D10EffectShaderResourceVariable::GetResourceArray
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
 - ID3D10EffectShaderResourceVariable.GetResourceArray
---

# ID3D10EffectShaderResourceVariable::GetResourceArray


## -description

Get an array of shader resources.

## -parameters

### -param ppResources [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>**</b>

The address of an array of shader-resource-view interfaces. See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView Interface</a>.

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

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>