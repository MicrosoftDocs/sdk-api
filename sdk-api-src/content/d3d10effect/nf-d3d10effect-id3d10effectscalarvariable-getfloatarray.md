---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.GetFloatArray
title: ID3D10EffectScalarVariable::GetFloatArray (d3d10effect.h)
description: Get an array of floating-point variables.
helpviewer_keywords: ["GetFloatArray","GetFloatArray method [Direct3D 10]","GetFloatArray method [Direct3D 10]","ID3D10EffectScalarVariable interface","ID3D10EffectScalarVariable interface [Direct3D 10]","GetFloatArray method","ID3D10EffectScalarVariable.GetFloatArray","ID3D10EffectScalarVariable::GetFloatArray","d3d10effect/ID3D10EffectScalarVariable::GetFloatArray","direct3d10.id3d10effectscalarvariable_getfloatarray","e8606cb9-74af-2b45-f488-1115ae3ccba4"]
old-location: direct3d10\id3d10effectscalarvariable_getfloatarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_getfloatarray.htm
ms.date: 12/05/2018
ms.keywords: GetFloatArray, GetFloatArray method [Direct3D 10], GetFloatArray method [Direct3D 10],ID3D10EffectScalarVariable interface, ID3D10EffectScalarVariable interface [Direct3D 10],GetFloatArray method, ID3D10EffectScalarVariable.GetFloatArray, ID3D10EffectScalarVariable::GetFloatArray, d3d10effect/ID3D10EffectScalarVariable::GetFloatArray, direct3d10.id3d10effectscalarvariable_getfloatarray, e8606cb9-74af-2b45-f488-1115ae3ccba4
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
 - ID3D10EffectScalarVariable::GetFloatArray
 - d3d10effect/ID3D10EffectScalarVariable::GetFloatArray
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
 - ID3D10EffectScalarVariable.GetFloatArray
---

# ID3D10EffectScalarVariable::GetFloatArray


## -description

Get an array of floating-point variables.

## -parameters

### -param pData [out]

Type: <b>float*</b>

A pointer to the start of the data to set.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Must be set to 0; this is reserved for future use.

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of array elements to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectscalarvariable">ID3D10EffectScalarVariable Interface</a>