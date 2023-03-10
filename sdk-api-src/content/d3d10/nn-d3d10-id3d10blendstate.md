---
UID: NN:d3d10.ID3D10BlendState
title: ID3D10BlendState (d3d10.h)
description: This blend-state interface accesses blending state for a Direct3D 10.0 device for the output-merger stage.
helpviewer_keywords: ["ID3D10BlendState","ID3D10BlendState interface [Direct3D 10]","ID3D10BlendState interface [Direct3D 10]","described","d3d10/ID3D10BlendState","direct3d10.id3d10blendstate","e7edf841-099a-0302-cacb-da34c915ac4c"]
old-location: direct3d10\id3d10blendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blendstate.htm
ms.date: 12/05/2018
ms.keywords: ID3D10BlendState, ID3D10BlendState interface [Direct3D 10], ID3D10BlendState interface [Direct3D 10],described, d3d10/ID3D10BlendState, direct3d10.id3d10blendstate, e7edf841-099a-0302-cacb-da34c915ac4c
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
 - ID3D10BlendState
 - d3d10/ID3D10BlendState
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
 - ID3D10BlendState
---

# ID3D10BlendState interface


## -description

This blend-state interface accesses blending state for a Direct3D 10.0 device for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger</a> stage.

## -inheritance

The <b>ID3D10BlendState</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10BlendState</b> also has these types of members:

## -remarks

Blending combines two pixel values. You have control over how the pixels are blended by using a predefined set of blending operations, as well as preblending operations. The <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">Blending Block Diagram</a> shows conceptually how blending works.

To create a blend-state interface, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createblendstate">ID3D10Device::CreateBlendState</a>. To initialize the blend state, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
