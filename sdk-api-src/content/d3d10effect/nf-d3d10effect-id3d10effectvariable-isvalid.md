---
UID: NF:d3d10effect.ID3D10EffectVariable.IsValid
title: ID3D10EffectVariable::IsValid (d3d10effect.h)
description: Compare the data type with the data stored.
helpviewer_keywords: ["ID3D10EffectVariable interface [Direct3D 10]","IsValid method","ID3D10EffectVariable.IsValid","ID3D10EffectVariable::IsValid","IsValid","IsValid method [Direct3D 10]","IsValid method [Direct3D 10]","ID3D10EffectVariable interface","b6f93adf-228e-7f53-1caf-9b813e3b0811","d3d10effect/ID3D10EffectVariable::IsValid","direct3d10.id3d10effectvariable_isvalid"]
old-location: direct3d10\id3d10effectvariable_isvalid.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_isvalid.htm
ms.date: 12/05/2018
ms.keywords: ID3D10EffectVariable interface [Direct3D 10],IsValid method, ID3D10EffectVariable.IsValid, ID3D10EffectVariable::IsValid, IsValid, IsValid method [Direct3D 10], IsValid method [Direct3D 10],ID3D10EffectVariable interface, b6f93adf-228e-7f53-1caf-9b813e3b0811, d3d10effect/ID3D10EffectVariable::IsValid, direct3d10.id3d10effectvariable_isvalid
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
 - ID3D10EffectVariable::IsValid
 - d3d10effect/ID3D10EffectVariable::IsValid
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
 - ID3D10EffectVariable.IsValid
---

# ID3D10EffectVariable::IsValid


## -description

Compare the data type with the data stored.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the syntax is valid; otherwise <b>FALSE</b>.

## -remarks

This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
