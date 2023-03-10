---
UID: NN:d3d11_3.ID3D11RenderTargetView1
title: ID3D11RenderTargetView1 (d3d11_3.h)
description: A render-target-view interface represents the render-target subresources that can be accessed during rendering.
helpviewer_keywords: ["ID3D11RenderTargetView1","ID3D11RenderTargetView1 interface [Direct3D 11]","ID3D11RenderTargetView1 interface [Direct3D 11]","described","d3d11_3/ID3D11RenderTargetView1","direct3d11.id3d11rendertargetview1"]
old-location: direct3d11\id3d11rendertargetview1.htm
tech.root: direct3d11
ms.assetid: 6063229D-A85A-46E8-9034-D1C2C26A5274
ms.date: 12/05/2018
ms.keywords: ID3D11RenderTargetView1, ID3D11RenderTargetView1 interface [Direct3D 11], ID3D11RenderTargetView1 interface [Direct3D 11],described, d3d11_3/ID3D11RenderTargetView1, direct3d11.id3d11rendertargetview1
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11RenderTargetView1
 - d3d11_3/ID3D11RenderTargetView1
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
 - ID3D11RenderTargetView1
---

# ID3D11RenderTargetView1 interface


## -description

A render-target-view interface represents the render-target subresources that can be accessed during rendering.

## -inheritance

The <b>ID3D11RenderTargetView1</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>. <b>ID3D11RenderTargetView1</b> also has these types of members:

## -remarks

To create a render-target view, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createrendertargetview1">ID3D11Device3::CreateRenderTargetView1</a>. To bind a render-target view to the pipeline, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.

A render target is a resource that can be written by the output-merger stage at the end of a render pass. Each render target can also have a corresponding depth-stencil view.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
