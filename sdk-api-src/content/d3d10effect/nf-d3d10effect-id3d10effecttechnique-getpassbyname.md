---
UID: NF:d3d10effect.ID3D10EffectTechnique.GetPassByName
title: ID3D10EffectTechnique::GetPassByName (d3d10effect.h)
description: Get a pass by name.
helpviewer_keywords: ["35788dc3-3901-8ccb-116d-9dbd8ac5f484","GetPassByName","GetPassByName method [Direct3D 10]","GetPassByName method [Direct3D 10]","ID3D10EffectTechnique interface","ID3D10EffectTechnique interface [Direct3D 10]","GetPassByName method","ID3D10EffectTechnique.GetPassByName","ID3D10EffectTechnique::GetPassByName","d3d10effect/ID3D10EffectTechnique::GetPassByName","direct3d10.id3d10effecttechnique_getpassbyname"]
old-location: direct3d10\id3d10effecttechnique_getpassbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttechnique_getpassbyname.htm
ms.date: 12/05/2018
ms.keywords: 35788dc3-3901-8ccb-116d-9dbd8ac5f484, GetPassByName, GetPassByName method [Direct3D 10], GetPassByName method [Direct3D 10],ID3D10EffectTechnique interface, ID3D10EffectTechnique interface [Direct3D 10],GetPassByName method, ID3D10EffectTechnique.GetPassByName, ID3D10EffectTechnique::GetPassByName, d3d10effect/ID3D10EffectTechnique::GetPassByName, direct3d10.id3d10effecttechnique_getpassbyname
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
 - ID3D10EffectTechnique::GetPassByName
 - d3d10effect/ID3D10EffectTechnique::GetPassByName
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
 - ID3D10EffectTechnique.GetPassByName
---

# ID3D10EffectTechnique::GetPassByName


## -description

Get a pass by name.

## -parameters

### -param Name [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the pass.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass Interface</a>.

## -remarks

A technique contains one or more passes; get a pass using a name or an index.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effecttechnique">ID3D10EffectTechnique Interface</a>