---
UID: NN:d3d10effect.ID3D10EffectConstantBuffer
title: ID3D10EffectConstantBuffer (d3d10effect.h)
description: A constant-buffer interface accesses constant buffers or texture buffers.
helpviewer_keywords: ["03babb38-8c88-954d-43c3-eb8942a15d5a","ID3D10EffectConstantBuffer","ID3D10EffectConstantBuffer interface [Direct3D 10]","ID3D10EffectConstantBuffer interface [Direct3D 10]","described","d3d10effect/ID3D10EffectConstantBuffer","direct3d10.id3d10effectconstantbuffer"]
old-location: direct3d10\id3d10effectconstantbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectconstantbuffer.htm
ms.date: 12/05/2018
ms.keywords: 03babb38-8c88-954d-43c3-eb8942a15d5a, ID3D10EffectConstantBuffer, ID3D10EffectConstantBuffer interface [Direct3D 10], ID3D10EffectConstantBuffer interface [Direct3D 10],described, d3d10effect/ID3D10EffectConstantBuffer, direct3d10.id3d10effectconstantbuffer
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectConstantBuffer
 - d3d10effect/ID3D10EffectConstantBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10EffectConstantBuffer
---

# ID3D10EffectConstantBuffer interface


## -description

A constant-buffer interface accesses constant buffers or texture buffers.

## -inheritance

The <b>ID3D10EffectConstantBuffer</b> interface inherits from <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>. <b>ID3D10EffectConstantBuffer</b> also has these types of members:

## -remarks

Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update. This allows you to minimize the number of state changes as well as make the fewest API calls to change state. Both of these factors lead to better performance.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>



<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectvariable">ID3D10EffectVariable</a>
