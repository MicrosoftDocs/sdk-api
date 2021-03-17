---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.SetMatrixTransposeArray
title: ID3D10EffectMatrixVariable::SetMatrixTransposeArray (d3d10effect.h)
description: Transpose and set an array of floating-point matrices.
helpviewer_keywords: ["ID3D10EffectMatrixVariable interface [Direct3D 10]","SetMatrixTransposeArray method","ID3D10EffectMatrixVariable.SetMatrixTransposeArray","ID3D10EffectMatrixVariable::SetMatrixTransposeArray","SetMatrixTransposeArray","SetMatrixTransposeArray method [Direct3D 10]","SetMatrixTransposeArray method [Direct3D 10]","ID3D10EffectMatrixVariable interface","cb946e9f-7956-c362-ead3-2f851b8fa74b","d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTransposeArray","direct3d10.id3d10effectmatrixvariable_setmatrixtransposearray"]
old-location: direct3d10\id3d10effectmatrixvariable_setmatrixtransposearray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_setmatrixtransposearray.htm
ms.date: 12/05/2018
ms.keywords: ID3D10EffectMatrixVariable interface [Direct3D 10],SetMatrixTransposeArray method, ID3D10EffectMatrixVariable.SetMatrixTransposeArray, ID3D10EffectMatrixVariable::SetMatrixTransposeArray, SetMatrixTransposeArray, SetMatrixTransposeArray method [Direct3D 10], SetMatrixTransposeArray method [Direct3D 10],ID3D10EffectMatrixVariable interface, cb946e9f-7956-c362-ead3-2f851b8fa74b, d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTransposeArray, direct3d10.id3d10effectmatrixvariable_setmatrixtransposearray
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
 - ID3D10EffectMatrixVariable::SetMatrixTransposeArray
 - d3d10effect/ID3D10EffectMatrixVariable::SetMatrixTransposeArray
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
 - ID3D10EffectMatrixVariable.SetMatrixTransposeArray
---

# ID3D10EffectMatrixVariable::SetMatrixTransposeArray


## -description

Transpose and set an array of floating-point matrices.

## -parameters

### -param pData [in]

Type: <b>float*</b>

A pointer to an array of matrices.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset (in number of matrices) between the start of the array and the first matrix to set.

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of matrices in the array to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectmatrixvariable">ID3D10EffectMatrixVariable Interface</a>