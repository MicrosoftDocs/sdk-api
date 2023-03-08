---
UID: NN:d3d10.ID3D10RasterizerState
title: ID3D10RasterizerState (d3d10.h)
description: A rasterizer-state interface accesses rasterizer state for the rasterizer stage.
helpviewer_keywords: ["ID3D10RasterizerState","ID3D10RasterizerState interface [Direct3D 10]","ID3D10RasterizerState interface [Direct3D 10]","described","ce1e96e6-707f-1c9e-1985-3b3acefd307f","d3d10/ID3D10RasterizerState","direct3d10.id3d10rasterizerstate"]
old-location: direct3d10\id3d10rasterizerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10rasterizerstate.htm
ms.date: 12/05/2018
ms.keywords: ID3D10RasterizerState, ID3D10RasterizerState interface [Direct3D 10], ID3D10RasterizerState interface [Direct3D 10],described, ce1e96e6-707f-1c9e-1985-3b3acefd307f, d3d10/ID3D10RasterizerState, direct3d10.id3d10rasterizerstate
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
 - ID3D10RasterizerState
 - d3d10/ID3D10RasterizerState
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
 - ID3D10RasterizerState
---

# ID3D10RasterizerState interface


## -description

A rasterizer-state interface accesses rasterizer state for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.

## -inheritance

The <b>ID3D10RasterizerState</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10RasterizerState</b> also has these types of members:

## -remarks

A rasterizer-state object is created with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrasterizerstate">ID3D10Device::CreateRasterizerState</a> and bound to the pipeline with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetstate">ID3D10Device::RSSetState</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
