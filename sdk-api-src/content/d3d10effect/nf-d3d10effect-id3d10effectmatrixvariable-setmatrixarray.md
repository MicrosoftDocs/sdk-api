---
UID: NF:d3d10effect.ID3D10EffectMatrixVariable.SetMatrixArray
title: ID3D10EffectMatrixVariable::SetMatrixArray (d3d10effect.h)
author: windows-sdk-content
description: Set an array of floating-point matrices.
old-location: direct3d10\id3d10effectmatrixvariable_setmatrixarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectmatrixvariable_setmatrixarray.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10EffectMatrixVariable interface [Direct3D 10],SetMatrixArray method, ID3D10EffectMatrixVariable.SetMatrixArray, ID3D10EffectMatrixVariable::SetMatrixArray, SetMatrixArray, SetMatrixArray method [Direct3D 10], SetMatrixArray method [Direct3D 10],ID3D10EffectMatrixVariable interface, ba745b53-173b-3f99-1c4a-10c74d10a02b, d3d10effect/ID3D10EffectMatrixVariable::SetMatrixArray, direct3d10.id3d10effectmatrixvariable_setmatrixarray
ms.topic: method
f1_keywords: ["d3d10effect/ID3D10EffectMatrixVariable.SetMatrixArray"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectMatrixVariable.SetMatrixArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectMatrixVariable::SetMatrixArray


## -description


Set an array of floating-point matrices.


## -parameters




### -param pData [in]

Type: <b>float*</b>

A pointer to the first matrix.


### -param Offset [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of matrix elements to skip from the start of the array.


### -param Count [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements to set.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectmatrixvariable">ID3D10EffectMatrixVariable Interface</a>
 

 

