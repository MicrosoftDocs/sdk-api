---
UID: NN:d3d11.ID3D11BlendState
title: ID3D11BlendState (d3d11.h)
description: The blend-state interface holds a description for blending state that you can bind to the output-merger stage.
helpviewer_keywords: ["888911a9-f093-b7b1-a4c3-e9f05bd39107","ID3D11BlendState","ID3D11BlendState interface [Direct3D 11]","ID3D11BlendState interface [Direct3D 11]","described","d3d11/ID3D11BlendState","direct3d11.id3d11blendstate"]
old-location: direct3d11\id3d11blendstate.htm
tech.root: direct3d11
ms.assetid: ccb39c89-eba7-473c-8358-dc3513da4be7
ms.date: 12/05/2018
ms.keywords: 888911a9-f093-b7b1-a4c3-e9f05bd39107, ID3D11BlendState, ID3D11BlendState interface [Direct3D 11], ID3D11BlendState interface [Direct3D 11],described, d3d11/ID3D11BlendState, direct3d11.id3d11blendstate
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
 - ID3D11BlendState
 - d3d11/ID3D11BlendState
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
 - ID3D11BlendState
---

# ID3D11BlendState interface


## -description

The blend-state interface holds a description for blending state that you can bind to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

## -inheritance

The <b>ID3D11BlendState</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11BlendState</b> also has these types of members:

## -remarks

Blending applies a simple function to combine output values from a pixel shader with data in a render target. You have control over how the pixels are blended by using a predefined set of blending operations and preblending operations.

To create a blend-state object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createblendstate">ID3D11Device::CreateBlendState</a>. To bind the blend-state object to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">ID3D11DeviceContext::OMSetBlendState</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
