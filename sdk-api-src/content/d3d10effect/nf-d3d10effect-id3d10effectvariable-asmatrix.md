---
UID: NF:d3d10effect.ID3D10EffectVariable.AsMatrix
title: ID3D10EffectVariable::AsMatrix (d3d10effect.h)
description: Get a matrix variable.
helpviewer_keywords: ["AsMatrix","AsMatrix method [Direct3D 10]","AsMatrix method [Direct3D 10]","ID3D10EffectVariable interface","ID3D10EffectVariable interface [Direct3D 10]","AsMatrix method","ID3D10EffectVariable.AsMatrix","ID3D10EffectVariable::AsMatrix","d3d10effect/ID3D10EffectVariable::AsMatrix","dc6784cd-b78e-6390-1d7a-db0d3c27410b","direct3d10.id3d10effectvariable_asmatrix"]
old-location: direct3d10\id3d10effectvariable_asmatrix.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asmatrix.htm
ms.date: 12/05/2018
ms.keywords: AsMatrix, AsMatrix method [Direct3D 10], AsMatrix method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsMatrix method, ID3D10EffectVariable.AsMatrix, ID3D10EffectVariable::AsMatrix, d3d10effect/ID3D10EffectVariable::AsMatrix, dc6784cd-b78e-6390-1d7a-db0d3c27410b, direct3d10.id3d10effectvariable_asmatrix
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
 - ID3D10EffectVariable::AsMatrix
 - d3d10effect/ID3D10EffectVariable::AsMatrix
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
 - ID3D10EffectVariable.AsMatrix
---

# ID3D10EffectVariable::AsMatrix


## -description

Get a matrix variable.



## -returns

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectmatrixvariable">ID3D10EffectMatrixVariable</a>*</b>

A pointer to a matrix variable. See <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectmatrixvariable">ID3D10EffectMatrixVariable</a>.

## -remarks

AsMatrix returns a version of the effect variable that has been specialized to a matrix variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain matrix data.

Applications can test the returned object for validity by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectvariable-isvalid">IsValid</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable Interface</a>
