---
UID: NN:d3d10.ID3D10View
title: ID3D10View (d3d10.h)
description: A view interface specifies the parts of a resource the pipeline can access during rendering (see view).
helpviewer_keywords: ["ID3D10View","ID3D10View interface [Direct3D 10]","ID3D10View interface [Direct3D 10]","described","d3d10/ID3D10View","direct3d10.id3d10view","f36206a8-55f1-ac58-4818-8c308ce6e81f"]
old-location: direct3d10\id3d10view.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10view.htm
ms.date: 12/05/2018
ms.keywords: ID3D10View, ID3D10View interface [Direct3D 10], ID3D10View interface [Direct3D 10],described, d3d10/ID3D10View, direct3d10.id3d10view, f36206a8-55f1-ac58-4818-8c308ce6e81f
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
 - ID3D10View
 - d3d10/ID3D10View
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
 - ID3D10View
---

# ID3D10View interface


## -description

A view interface specifies the parts of a resource the pipeline can access during rendering (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a>).

## -inheritance

The <b>ID3D10View</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10View</b> also has these types of members:

## -remarks

A view interface is the base interface for all views. There are three types of views; a depth-stencil view, a render-target view, and a shader-resource view.

<ul>
<li>To create a render-target view, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>.</li>
<li>To create a depth-stencil view, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>.</li>
<li>To create a shader-resource view, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.</li>
</ul>
All resources must be bound to the pipeline before they can be accessed.

<ul>
<li>To bind a render-target view or a depth-stencil view, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">ID3D10Device::OMSetRenderTargets</a>.</li>
<li>To bind a shader-resource view, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">ID3D10Device::VSSetShaderResources</a>.</li>
</ul>
A view can also be used to access a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">typeless resource</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
