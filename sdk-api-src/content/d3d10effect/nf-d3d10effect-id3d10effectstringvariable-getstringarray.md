---
UID: NF:d3d10effect.ID3D10EffectStringVariable.GetStringArray
title: ID3D10EffectStringVariable::GetStringArray (d3d10effect.h)
description: Get an array of strings.
helpviewer_keywords: ["3a4b3089-4ba1-9479-73b6-84f4d49b52d8","GetStringArray","GetStringArray method [Direct3D 10]","GetStringArray method [Direct3D 10]","ID3D10EffectStringVariable interface","ID3D10EffectStringVariable interface [Direct3D 10]","GetStringArray method","ID3D10EffectStringVariable.GetStringArray","ID3D10EffectStringVariable::GetStringArray","d3d10effect/ID3D10EffectStringVariable::GetStringArray","direct3d10.id3d10effectstringvariable_getstringarray"]
old-location: direct3d10\id3d10effectstringvariable_getstringarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectstringvariable_getstringarray.htm
ms.date: 12/05/2018
ms.keywords: 3a4b3089-4ba1-9479-73b6-84f4d49b52d8, GetStringArray, GetStringArray method [Direct3D 10], GetStringArray method [Direct3D 10],ID3D10EffectStringVariable interface, ID3D10EffectStringVariable interface [Direct3D 10],GetStringArray method, ID3D10EffectStringVariable.GetStringArray, ID3D10EffectStringVariable::GetStringArray, d3d10effect/ID3D10EffectStringVariable::GetStringArray, direct3d10.id3d10effectstringvariable_getstringarray
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
 - ID3D10EffectStringVariable::GetStringArray
 - d3d10effect/ID3D10EffectStringVariable::GetStringArray
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
 - ID3D10EffectStringVariable.GetStringArray
---

# ID3D10EffectStringVariable::GetStringArray


## -description

Get an array of strings.

## -parameters

### -param ppStrings [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a>*</b>

A pointer to the first string in the array.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset (in number of strings) between the start of the array and the first string to get.

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of strings in the returned array.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectstringvariable">ID3D10EffectStringVariable Interface</a>