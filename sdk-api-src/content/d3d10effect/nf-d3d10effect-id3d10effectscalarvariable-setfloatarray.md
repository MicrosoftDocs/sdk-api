---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.SetFloatArray
title: ID3D10EffectScalarVariable::SetFloatArray (d3d10effect.h)
description: Set an array of floating-point variables.
helpviewer_keywords: ["028a02f1-2ddd-f6aa-b520-88cbdd70c9d3","ID3D10EffectScalarVariable interface [Direct3D 10]","SetFloatArray method","ID3D10EffectScalarVariable.SetFloatArray","ID3D10EffectScalarVariable::SetFloatArray","SetFloatArray","SetFloatArray method [Direct3D 10]","SetFloatArray method [Direct3D 10]","ID3D10EffectScalarVariable interface","d3d10effect/ID3D10EffectScalarVariable::SetFloatArray","direct3d10.id3d10effectscalarvariable_setfloatarray"]
old-location: direct3d10\id3d10effectscalarvariable_setfloatarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_setfloatarray.htm
ms.date: 12/05/2018
ms.keywords: 028a02f1-2ddd-f6aa-b520-88cbdd70c9d3, ID3D10EffectScalarVariable interface [Direct3D 10],SetFloatArray method, ID3D10EffectScalarVariable.SetFloatArray, ID3D10EffectScalarVariable::SetFloatArray, SetFloatArray, SetFloatArray method [Direct3D 10], SetFloatArray method [Direct3D 10],ID3D10EffectScalarVariable interface, d3d10effect/ID3D10EffectScalarVariable::SetFloatArray, direct3d10.id3d10effectscalarvariable_setfloatarray
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
 - ID3D10EffectScalarVariable::SetFloatArray
 - d3d10effect/ID3D10EffectScalarVariable::SetFloatArray
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
 - ID3D10EffectScalarVariable.SetFloatArray
---

# ID3D10EffectScalarVariable::SetFloatArray


## -description

Set an array of floating-point variables.

## -parameters

### -param pData [in]

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