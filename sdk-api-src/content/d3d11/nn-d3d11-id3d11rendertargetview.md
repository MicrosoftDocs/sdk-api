---
UID: NN:d3d11.ID3D11RenderTargetView
title: ID3D11RenderTargetView (d3d11.h)
description: A render-target-view interface identifies the render-target subresources that can be accessed during rendering. (ID3D11RenderTargetView)
helpviewer_keywords: ["ID3D11RenderTargetView","ID3D11RenderTargetView interface [Direct3D 11]","ID3D11RenderTargetView interface [Direct3D 11]","described","d3d11/ID3D11RenderTargetView","direct3d11.id3d11rendertargetview","ffd3acf9-f2dc-0823-23c9-1188e5ede6f2"]
old-location: direct3d11\id3d11rendertargetview.htm
tech.root: direct3d11
ms.assetid: 3ae7c255-2403-493a-9fb9-fc9795f6d920
ms.date: 12/05/2018
ms.keywords: ID3D11RenderTargetView, ID3D11RenderTargetView interface [Direct3D 11], ID3D11RenderTargetView interface [Direct3D 11],described, d3d11/ID3D11RenderTargetView, direct3d11.id3d11rendertargetview, ffd3acf9-f2dc-0823-23c9-1188e5ede6f2
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
 - ID3D11RenderTargetView
 - d3d11/ID3D11RenderTargetView
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
 - ID3D11RenderTargetView
---

# ID3D11RenderTargetView interface


## -description

A render-target-view interface identifies the render-target subresources that can be accessed during rendering.

## -inheritance

The <b>ID3D11RenderTargetView</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>. <b>ID3D11RenderTargetView</b> also has these types of members:

## -remarks

To create a render-target view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">ID3D11Device::CreateRenderTargetView</a>. To bind a render-target view to the pipeline, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.

A rendertarget is a resource that can be written by the output-merger stage at the end of a render pass. Each render-target should also have a corresponding depth-stencil view.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
