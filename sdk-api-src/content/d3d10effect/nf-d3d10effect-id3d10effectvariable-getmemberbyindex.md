---
UID: NF:d3d10effect.ID3D10EffectVariable.GetMemberByIndex
title: ID3D10EffectVariable::GetMemberByIndex (d3d10effect.h)
description: Get a structure member by index.
helpviewer_keywords: ["GetMemberByIndex","GetMemberByIndex method [Direct3D 10]","GetMemberByIndex method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetMemberByIndex method","ID3D10EffectVariable.GetMemberByIndex","ID3D10EffectVariable::GetMemberByIndex","d3d10effect/ID3D10EffectVariable::GetMemberByIndex","direct3d10.id3d10effectvariable_getmemberbyindex","fa133b0d-50ce-9480-c0e6-b65721679e9d"]
old-location: direct3d10\id3d10effectvariable_getmemberbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getmemberbyindex.htm
ms.date: 12/05/2018
ms.keywords: GetMemberByIndex, GetMemberByIndex method [Direct3D 10], GetMemberByIndex method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetMemberByIndex method, ID3D10EffectVariable.GetMemberByIndex, ID3D10EffectVariable::GetMemberByIndex, d3d10effect/ID3D10EffectVariable::GetMemberByIndex, direct3d10.id3d10effectvariable_getmemberbyindex, fa133b0d-50ce-9480-c0e6-b65721679e9d
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
 - ID3D10EffectVariable::GetMemberByIndex
 - d3d10effect/ID3D10EffectVariable::GetMemberByIndex
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
 - ID3D10EffectVariable.GetMemberByIndex
---

# ID3D10EffectVariable::GetMemberByIndex


## -description

Get a structure member by index.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

If the effect variable is a structure, use this method to look up a member by index.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>