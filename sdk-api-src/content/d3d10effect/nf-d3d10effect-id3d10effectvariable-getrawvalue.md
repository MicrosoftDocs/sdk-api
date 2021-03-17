---
UID: NF:d3d10effect.ID3D10EffectVariable.GetRawValue
title: ID3D10EffectVariable::GetRawValue (d3d10effect.h)
description: Get data.
helpviewer_keywords: ["18ba7994-4337-bf43-0492-e591b629b77d","GetRawValue","GetRawValue method [Direct3D 10]","GetRawValue method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetRawValue method","ID3D10EffectVariable.GetRawValue","ID3D10EffectVariable::GetRawValue","d3d10effect/ID3D10EffectVariable::GetRawValue","direct3d10.id3d10effectvariable_getrawvalue"]
old-location: direct3d10\id3d10effectvariable_getrawvalue.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getrawvalue.htm
ms.date: 12/05/2018
ms.keywords: 18ba7994-4337-bf43-0492-e591b629b77d, GetRawValue, GetRawValue method [Direct3D 10], GetRawValue method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetRawValue method, ID3D10EffectVariable.GetRawValue, ID3D10EffectVariable::GetRawValue, d3d10effect/ID3D10EffectVariable::GetRawValue, direct3d10.id3d10effectvariable_getrawvalue
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
 - ID3D10EffectVariable::GetRawValue
 - d3d10effect/ID3D10EffectVariable::GetRawValue
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
 - ID3D10EffectVariable.GetRawValue
---

# ID3D10EffectVariable::GetRawValue


## -description

Get data.

## -parameters

### -param pData [in]

Type: <b>void*</b>

A pointer to the variable.

### -param Offset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset (in bytes) from the beginning of the pointer to the data.

### -param ByteCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of bytes to get.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This method does no conversion or type checking; it is therefore a very quick way to access array items.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>