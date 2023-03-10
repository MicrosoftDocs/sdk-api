---
UID: NF:d3d10effect.ID3D10EffectShaderResourceVariable.SetResourceArray
title: ID3D10EffectShaderResourceVariable::SetResourceArray (d3d10effect.h)
description: Set an array of shader resources.
helpviewer_keywords: ["ID3D10EffectShaderResourceVariable interface [Direct3D 10]","SetResourceArray method","ID3D10EffectShaderResourceVariable.SetResourceArray","ID3D10EffectShaderResourceVariable::SetResourceArray","SetResourceArray","SetResourceArray method [Direct3D 10]","SetResourceArray method [Direct3D 10]","ID3D10EffectShaderResourceVariable interface","d3d10effect/ID3D10EffectShaderResourceVariable::SetResourceArray","direct3d10.id3d10effectshaderresourcevariable_setresourcearray","ffaa0326-c3e6-873d-a783-a06195e76351"]
old-location: direct3d10\id3d10effectshaderresourcevariable_setresourcearray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshaderresourcevariable_setresourcearray.htm
ms.date: 12/05/2018
ms.keywords: ID3D10EffectShaderResourceVariable interface [Direct3D 10],SetResourceArray method, ID3D10EffectShaderResourceVariable.SetResourceArray, ID3D10EffectShaderResourceVariable::SetResourceArray, SetResourceArray, SetResourceArray method [Direct3D 10], SetResourceArray method [Direct3D 10],ID3D10EffectShaderResourceVariable interface, d3d10effect/ID3D10EffectShaderResourceVariable::SetResourceArray, direct3d10.id3d10effectshaderresourcevariable_setresourcearray, ffaa0326-c3e6-873d-a783-a06195e76351
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
 - ID3D10EffectShaderResourceVariable::SetResourceArray
 - d3d10effect/ID3D10EffectShaderResourceVariable::SetResourceArray
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
 - ID3D10EffectShaderResourceVariable.SetResourceArray
---

# ID3D10EffectShaderResourceVariable::SetResourceArray


## -description

Set an array of shader resources.

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