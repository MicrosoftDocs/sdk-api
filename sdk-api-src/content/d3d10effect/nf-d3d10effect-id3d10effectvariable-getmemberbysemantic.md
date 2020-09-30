---
UID: NF:d3d10effect.ID3D10EffectVariable.GetMemberBySemantic
title: ID3D10EffectVariable::GetMemberBySemantic (d3d10effect.h)
description: Get a structure member by semantic.
helpviewer_keywords: ["39fcf4c4-6072-0377-d1b8-ca11cc848a0c","GetMemberBySemantic","GetMemberBySemantic method [Direct3D 10]","GetMemberBySemantic method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","GetMemberBySemantic method","ID3D10EffectVariable.GetMemberBySemantic","ID3D10EffectVariable::GetMemberBySemantic","d3d10effect/ID3D10EffectVariable::GetMemberBySemantic","direct3d10.id3d10effectvariable_getmemberbysemantic"]
old-location: direct3d10\id3d10effectvariable_getmemberbysemantic.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getmemberbysemantic.htm
ms.date: 12/05/2018
ms.keywords: 39fcf4c4-6072-0377-d1b8-ca11cc848a0c, GetMemberBySemantic, GetMemberBySemantic method [Direct3D 10], GetMemberBySemantic method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetMemberBySemantic method, ID3D10EffectVariable.GetMemberBySemantic, ID3D10EffectVariable::GetMemberBySemantic, d3d10effect/ID3D10EffectVariable::GetMemberBySemantic, direct3d10.id3d10effectvariable_getmemberbysemantic
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
 - ID3D10EffectVariable::GetMemberBySemantic
 - d3d10effect/ID3D10EffectVariable::GetMemberBySemantic
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
 - ID3D10EffectVariable.GetMemberBySemantic
---

# ID3D10EffectVariable::GetMemberBySemantic


## -description

Get a structure member by semantic.

## -parameters

### -param Semantic [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The semantic.

## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>.

## -remarks

If the effect variable is an structure, use this method to look up a member by attached semantic.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>