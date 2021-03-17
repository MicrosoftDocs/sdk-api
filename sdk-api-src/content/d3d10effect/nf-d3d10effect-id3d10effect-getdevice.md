---
UID: NF:d3d10effect.ID3D10Effect.GetDevice
title: ID3D10Effect::GetDevice (d3d10effect.h)
description: Get the device that created the effect.
helpviewer_keywords: ["92eb984e-62b3-6a6f-ab2b-93b561a93fc3","GetDevice","GetDevice method [Direct3D 10]","GetDevice method [Direct3D 10]","ID3D10Effect interface","ID3D10Effect interface [Direct3D 10]","GetDevice method","ID3D10Effect.GetDevice","ID3D10Effect::GetDevice","d3d10effect/ID3D10Effect::GetDevice","direct3d10.id3d10effect_getdevice"]
old-location: direct3d10\id3d10effect_getdevice.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getdevice.htm
ms.date: 12/05/2018
ms.keywords: 92eb984e-62b3-6a6f-ab2b-93b561a93fc3, GetDevice, GetDevice method [Direct3D 10], GetDevice method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetDevice method, ID3D10Effect.GetDevice, ID3D10Effect::GetDevice, d3d10effect/ID3D10Effect::GetDevice, direct3d10.id3d10effect_getdevice
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
 - ID3D10Effect::GetDevice
 - d3d10effect/ID3D10Effect::GetDevice
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
 - ID3D10Effect.GetDevice
---

# ID3D10Effect::GetDevice


## -description

Get the device that created the effect.

## -parameters

### -param ppDevice [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>**</b>

A pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An effect is created for a specific device, by calling a function such as <a href="/windows/desktop/direct3d10/d3dx10createeffectfromfile">D3DX10CreateEffectFromFile</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>