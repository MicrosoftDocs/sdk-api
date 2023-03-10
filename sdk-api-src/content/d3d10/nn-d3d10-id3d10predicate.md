---
UID: NN:d3d10.ID3D10Predicate
title: ID3D10Predicate (d3d10.h)
description: A predicate interface determines whether geometry should be processed depending on the results of a previous draw call. (ID3D10Predicate)
helpviewer_keywords: ["350beb86-4869-80f7-d757-00ebb1191143","ID3D10Predicate","ID3D10Predicate interface [Direct3D 10]","ID3D10Predicate interface [Direct3D 10]","described","d3d10/ID3D10Predicate","direct3d10.id3d10predicate"]
old-location: direct3d10\id3d10predicate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10predicate.htm
ms.date: 12/05/2018
ms.keywords: 350beb86-4869-80f7-d757-00ebb1191143, ID3D10Predicate, ID3D10Predicate interface [Direct3D 10], ID3D10Predicate interface [Direct3D 10],described, d3d10/ID3D10Predicate, direct3d10.id3d10predicate
req.header: d3d10.h
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
 - ID3D10Predicate
 - d3d10/ID3D10Predicate
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
 - ID3D10Predicate
---

# ID3D10Predicate interface


## -description

A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.

## -remarks

A predicate can be created with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createpredicate">ID3D10Device::CreatePredicate</a>, and used with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setpredication">ID3D10Device::SetPredication</a>.

There are two types of predicates in Direct3D 10: stream-output-overflow predicates and occlusion predicates. Stream-output-overflow predicates will cause any geometry residing in stream-output buffers that were overflowed to not be processed. Occlusion predicates will cause any geometry that did not have a single sample pass the depth/stencil tests to not be processed.

For an example of occlusion-predicated rendering, see <a href="https://msdn.microsoft.com/library/Ee416402(v=VS.85).aspx">Draw Predicated Sample</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10query">ID3D10Query</a>
