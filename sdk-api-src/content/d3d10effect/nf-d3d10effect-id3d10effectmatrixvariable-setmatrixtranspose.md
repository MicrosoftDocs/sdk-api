---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.SetMatrixTranspose
title: ID3D10EffectMatrixVariable::SetMatrixTranspose (d3d10effect.h)
description: Transpose and set a floating-point matrix.
helpviewer_keywords: ["8561664e-7026-5fcc-43aa-11163abdb56f","ID3D10EffectMatrixVariable interface [Direct3D 10]","SetMatrixTranspose method","ID3D10EffectMatrixVariable.SetMatrixTranspose","ID3D10EffectMatrixVariable::SetMatrixTranspose","SetMatrixTranspose","SetMatrixTranspose method [Direct3D 10]","SetMatrixTranspose method [Direct3D 10]","ID3D10EffectMatrixVariable interface","d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTranspose","direct3d10.id3d10effectmatrixvariable_setmatrixtranspose"]
old-location: direct3d10\id3d10effectmatrixvariable_setmatrixtranspose.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_setmatrixtranspose.htm
ms.date: 12/05/2018
ms.keywords: 8561664e-7026-5fcc-43aa-11163abdb56f, ID3D10EffectMatrixVariable interface [Direct3D 10],SetMatrixTranspose method, ID3D10EffectMatrixVariable.SetMatrixTranspose, ID3D10EffectMatrixVariable::SetMatrixTranspose, SetMatrixTranspose, SetMatrixTranspose method [Direct3D 10], SetMatrixTranspose method [Direct3D 10],ID3D10EffectMatrixVariable interface, d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTranspose, direct3d10.id3d10effectmatrixvariable_setmatrixtranspose
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
 - ID3D10EffectMatrixVariable::SetMatrixTranspose
 - d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTranspose
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
 - ID3D10EffectMatrixVariable.SetMatrixTranspose
---

# ID3D10EffectMatrixVariable::SetMatrixTranspose


## -description

Transpose and set a floating-point matrix.

## -parameters

### -param pData [in]

Type: <b>float*</b>

A pointer to the first element of a matrix.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectmatrixvariable">ID3D10EffectMatrixVariable Interface</a>