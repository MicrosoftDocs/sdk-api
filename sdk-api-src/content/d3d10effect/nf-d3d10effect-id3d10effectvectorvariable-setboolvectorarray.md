---
UID: NF:d3d10effect.ID3D10EffectVectorVariable.SetBoolVectorArray
title: ID3D10EffectVectorVariable::SetBoolVectorArray (d3d10effect.h)
description: Set an array of four-component vectors that contain boolean data.
helpviewer_keywords: ["ID3D10EffectVectorVariable interface [Direct3D 10]","SetBoolVectorArray method","ID3D10EffectVectorVariable.SetBoolVectorArray","ID3D10EffectVectorVariable::SetBoolVectorArray","SetBoolVectorArray","SetBoolVectorArray method [Direct3D 10]","SetBoolVectorArray method [Direct3D 10]","ID3D10EffectVectorVariable interface","d3d10effect/ID3D10EffectVectorVariable::SetBoolVectorArray","d898b40d-7046-3bfa-967a-dd167091c829","direct3d10.id3d10effectvectorvariable_setboolvectorarray"]
old-location: direct3d10\id3d10effectvectorvariable_setboolvectorarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvectorvariable_setboolvectorarray.htm
ms.date: 12/05/2018
ms.keywords: ID3D10EffectVectorVariable interface [Direct3D 10],SetBoolVectorArray method, ID3D10EffectVectorVariable.SetBoolVectorArray, ID3D10EffectVectorVariable::SetBoolVectorArray, SetBoolVectorArray, SetBoolVectorArray method [Direct3D 10], SetBoolVectorArray method [Direct3D 10],ID3D10EffectVectorVariable interface, d3d10effect/ID3D10EffectVectorVariable::SetBoolVectorArray, d898b40d-7046-3bfa-967a-dd167091c829, direct3d10.id3d10effectvectorvariable_setboolvectorarray
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
 - ID3D10EffectVectorVariable::SetBoolVectorArray
 - d3d10effect/ID3D10EffectVectorVariable::SetBoolVectorArray
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
 - ID3D10EffectVectorVariable.SetBoolVectorArray
---

# ID3D10EffectVectorVariable::SetBoolVectorArray


## -description

Set an array of four-component vectors that contain boolean data.

## -parameters

### -param pData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

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

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvectorvariable">ID3D10EffectVectorVariable Interface</a>