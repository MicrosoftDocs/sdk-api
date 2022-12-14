---
UID: NN:d3d10.ID3D10DepthStencilState
title: ID3D10DepthStencilState (d3d10.h)
description: A depth-stencil-state interface accesses depth-stencil state which sets up the depth-stencil test for the output-merger stage.
helpviewer_keywords: ["756bea1e-80cb-6163-33a9-bbedb02e57da","ID3D10DepthStencilState","ID3D10DepthStencilState interface [Direct3D 10]","ID3D10DepthStencilState interface [Direct3D 10]","described","d3d10/ID3D10DepthStencilState","direct3d10.id3d10depthstencilstate"]
old-location: direct3d10\id3d10depthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10depthstencilstate.htm
ms.date: 12/05/2018
ms.keywords: 756bea1e-80cb-6163-33a9-bbedb02e57da, ID3D10DepthStencilState, ID3D10DepthStencilState interface [Direct3D 10], ID3D10DepthStencilState interface [Direct3D 10],described, d3d10/ID3D10DepthStencilState, direct3d10.id3d10depthstencilstate
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
 - ID3D10DepthStencilState
 - d3d10/ID3D10DepthStencilState
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
 - ID3D10DepthStencilState
---

# ID3D10DepthStencilState interface


## -description

A depth-stencil-state interface accesses depth-stencil state which sets up the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil test</a> for the output-merger stage.

## -inheritance

The <b>ID3D10DepthStencilState</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10DepthStencilState</b> also has these types of members:

## -remarks

Create a depth-stencil state object by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilstate">ID3D10Device::CreateDepthStencilState</a>.

To initialize depth-stencil state, bind the depth-stencil-state object to the pipeline by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetdepthstencilstate">ID3D10Device::OMSetDepthStencilState</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
