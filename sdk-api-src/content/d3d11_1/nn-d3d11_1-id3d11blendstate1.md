---
UID: NN:d3d11_1.ID3D11BlendState1
title: ID3D11BlendState1 (d3d11_1.h)
description: The blend-state interface holds a description for blending state that you can bind to the output-merger stage. This blend-state interface supports logical operations as well as blending operations.
helpviewer_keywords: ["ID3D11BlendState1","ID3D11BlendState1 interface [Direct3D 11]","ID3D11BlendState1 interface [Direct3D 11]","described","d3d11_1/ID3D11BlendState1","direct3d11.id3d11blendstate1"]
old-location: direct3d11\id3d11blendstate1.htm
tech.root: direct3d11
ms.assetid: 5562F0B2-77FC-4614-BFA9-077323D4A2FA
ms.date: 12/05/2018
ms.keywords: ID3D11BlendState1, ID3D11BlendState1 interface [Direct3D 11], ID3D11BlendState1 interface [Direct3D 11],described, d3d11_1/ID3D11BlendState1, direct3d11.id3d11blendstate1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11BlendState1
 - d3d11_1/ID3D11BlendState1
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
 - ID3D11BlendState1
---

# ID3D11BlendState1 interface


## -description

The blend-state interface holds a description for blending state that you can bind to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>. This blend-state interface supports logical operations as well as blending operations.

## -inheritance

The <b>ID3D11BlendState1</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>. <b>ID3D11BlendState1</b> also has these types of members:

## -remarks

Blending applies a simple function to combine output values from a pixel shader with data in a render target. You have control over how the pixels are blended by using a predefined set of blending operations and preblending operations.

To create a blend-state object, call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createblendstate1">ID3D11Device1::CreateBlendState1</a>. To bind the blend-state object to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">ID3D11DeviceContext::OMSetBlendState</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>
