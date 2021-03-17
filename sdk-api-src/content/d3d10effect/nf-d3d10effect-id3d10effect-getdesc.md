---
UID: NF:d3d10effect.ID3D10Effect.GetDesc
title: ID3D10Effect::GetDesc (d3d10effect.h)
description: Get an effect description.
helpviewer_keywords: ["35c1c99a-3f41-0efe-adae-ce9709830b32","GetDesc","GetDesc method [Direct3D 10]","GetDesc method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetDesc method","ID3D10Effect.GetDesc","ID3D10Effect::GetDesc","d3d10effect/ID3D10Effect::GetDesc","direct3d10.id3d10effect_getdesc"]
old-location: direct3d10\id3d10effect_getdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getdesc.htm
ms.date: 12/05/2018
ms.keywords: 35c1c99a-3f41-0efe-adae-ce9709830b32, GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetDesc method, ID3D10Effect.GetDesc, ID3D10Effect::GetDesc, d3d10effect/ID3D10Effect::GetDesc, direct3d10.id3d10effect_getdesc
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
 - ID3D10Effect::GetDesc
 - d3d10effect/ID3D10Effect::GetDesc
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
 - ID3D10Effect.GetDesc
---

# ID3D10Effect::GetDesc


## -description

Get an effect description.

## -parameters

### -param pDesc [in, out]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_effect_desc">D3D10_EFFECT_DESC</a>*</b>

A pointer to an effect description (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_effect_desc">D3D10_EFFECT_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>