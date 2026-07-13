---
UID: NN:d3d11.ID3D11Predicate
title: ID3D11Predicate (d3d11.h)
description: A predicate interface determines whether geometry should be processed depending on the results of a previous draw call. (ID3D11Predicate)
helpviewer_keywords: ["7bbde1c2-0bd3-3fda-2288-938ac2c04c3a","ID3D11Predicate","ID3D11Predicate interface [Direct3D 11]","ID3D11Predicate interface [Direct3D 11]","described","d3d11/ID3D11Predicate","direct3d11.id3d11predicate"]
old-location: direct3d11\id3d11predicate.htm
tech.root: direct3d11
ms.assetid: ad16e0ac-a5ff-41ae-9b73-e93235ef891b
ms.date: 12/05/2018
ms.keywords: 7bbde1c2-0bd3-3fda-2288-938ac2c04c3a, ID3D11Predicate, ID3D11Predicate interface [Direct3D 11], ID3D11Predicate interface [Direct3D 11],described, d3d11/ID3D11Predicate, direct3d11.id3d11predicate
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Predicate
 - d3d11/ID3D11Predicate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Predicate
---

# ID3D11Predicate interface


## -description

A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.

## -remarks

To create a predicate object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpredicate">ID3D11Device::CreatePredicate</a>. To set the predicate object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-setpredication">ID3D11DeviceContext::SetPredication</a>.

There are two types of predicates: stream-output-overflow predicates and occlusion predicates. Stream-output-overflow predicates cause any geometry residing in stream-output buffers that were overflowed to not be processed. Occlusion predicates cause any geometry that did not have a single sample pass the depth/stencil tests to not be processed.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a>
