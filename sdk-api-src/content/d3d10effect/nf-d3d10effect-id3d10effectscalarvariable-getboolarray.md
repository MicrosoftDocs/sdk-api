---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.GetBoolArray
title: ID3D10EffectScalarVariable::GetBoolArray (d3d10effect.h)
description: Get an array of boolean variables.
helpviewer_keywords: ["GetBoolArray","GetBoolArray method [Direct3D 10]","GetBoolArray method [Direct3D 10]","ID3D10EffectScalarVariable interface","ID3D10EffectScalarVariable interface [Direct3D 10]","GetBoolArray method","ID3D10EffectScalarVariable.GetBoolArray","ID3D10EffectScalarVariable::GetBoolArray","d3d10effect/ID3D10EffectScalarVariable::GetBoolArray","direct3d10.id3d10effectscalarvariable_getboolarray","fbddf130-1eef-5bad-8fad-819c89e5a371"]
old-location: direct3d10\id3d10effectscalarvariable_getboolarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_getboolarray.htm
ms.date: 12/05/2018
ms.keywords: GetBoolArray, GetBoolArray method [Direct3D 10], GetBoolArray method [Direct3D 10],ID3D10EffectScalarVariable interface, ID3D10EffectScalarVariable interface [Direct3D 10],GetBoolArray method, ID3D10EffectScalarVariable.GetBoolArray, ID3D10EffectScalarVariable::GetBoolArray, d3d10effect/ID3D10EffectScalarVariable::GetBoolArray, direct3d10.id3d10effectscalarvariable_getboolarray, fbddf130-1eef-5bad-8fad-819c89e5a371
f1_keywords:
- d3d10effect/ID3D10EffectScalarVariable.GetBoolArray
dev_langs:
- c++
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
- ID3D10EffectScalarVariable.GetBoolArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectScalarVariable::GetBoolArray


## -description


Get an array of boolean variables.


## -parameters




### -param pData [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

A pointer to the start of the data to set.


### -param Offset [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Must be set to 0; this is reserved for future use. 


### -param Count [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of array elements to set.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectscalarvariable">ID3D10EffectScalarVariable Interface</a>
 

 

