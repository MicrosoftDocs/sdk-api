---
UID: NN:d3d11.ID3D11DepthStencilView
title: ID3D11DepthStencilView (d3d11.h)
description: A depth-stencil-view interface accesses a texture resource during depth-stencil testing. (ID3D11DepthStencilView)
helpviewer_keywords: ["5e846266-8e0b-d52b-2f70-8936cbeb0bd1","ID3D11DepthStencilView","ID3D11DepthStencilView interface [Direct3D 11]","ID3D11DepthStencilView interface [Direct3D 11]","described","d3d11/ID3D11DepthStencilView","direct3d11.id3d11depthstencilview"]
old-location: direct3d11\id3d11depthstencilview.htm
tech.root: direct3d11
ms.assetid: 10be1fd1-8700-4c0a-b447-d3c2569f8e81
ms.date: 12/05/2018
ms.keywords: 5e846266-8e0b-d52b-2f70-8936cbeb0bd1, ID3D11DepthStencilView, ID3D11DepthStencilView interface [Direct3D 11], ID3D11DepthStencilView interface [Direct3D 11],described, d3d11/ID3D11DepthStencilView, direct3d11.id3d11depthstencilview
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
 - ID3D11DepthStencilView
 - d3d11/ID3D11DepthStencilView
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
 - ID3D11DepthStencilView
---

# ID3D11DepthStencilView interface


## -description

A depth-stencil-view interface accesses a texture resource during depth-stencil testing.

## -inheritance

The <b>ID3D11DepthStencilView</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>. <b>ID3D11DepthStencilView</b> also has these types of members:

## -remarks

To create a depth-stencil view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilview">ID3D11Device::CreateDepthStencilView</a>.

To bind a depth-stencil view to the pipeline, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
