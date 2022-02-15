---
UID: NN:d3d11.ID3D11RasterizerState
title: ID3D11RasterizerState (d3d11.h)
description: The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage.
helpviewer_keywords: ["6b2716ca-7676-6b26-071d-20ec80705737","ID3D11RasterizerState","ID3D11RasterizerState interface [Direct3D 11]","ID3D11RasterizerState interface [Direct3D 11]","described","d3d11/ID3D11RasterizerState","direct3d11.id3d11rasterizerstate"]
old-location: direct3d11\id3d11rasterizerstate.htm
tech.root: direct3d11
ms.assetid: fbe6d2b9-375e-4390-9d34-36acef0a5aa2
ms.date: 12/05/2018
ms.keywords: 6b2716ca-7676-6b26-071d-20ec80705737, ID3D11RasterizerState, ID3D11RasterizerState interface [Direct3D 11], ID3D11RasterizerState interface [Direct3D 11],described, d3d11/ID3D11RasterizerState, direct3d11.id3d11rasterizerstate
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
 - ID3D11RasterizerState
 - d3d11/ID3D11RasterizerState
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
 - ID3D11RasterizerState
---

# ID3D11RasterizerState interface


## -description

The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.

## -inheritance

The <b>ID3D11RasterizerState</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11RasterizerState</b> also has these types of members:

## -remarks

To create a rasterizer-state object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrasterizerstate">ID3D11Device::CreateRasterizerState</a>. To bind the rasterizer-state object to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">ID3D11DeviceContext::RSSetState</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
