---
UID: NN:d3d11.ID3D11View
title: ID3D11View (d3d11.h)
description: A view interface specifies the parts of a resource the pipeline can access during rendering. (ID3D11View)
helpviewer_keywords: ["0332b528-6d94-2603-1e1b-65d4d541f94f","ID3D11View","ID3D11View interface [Direct3D 11]","ID3D11View interface [Direct3D 11]","described","d3d11/ID3D11View","direct3d11.id3d11view"]
old-location: direct3d11\id3d11view.htm
tech.root: direct3d11
ms.assetid: 060973b4-bf7d-4be2-b087-85a5b1bca905
ms.date: 12/05/2018
ms.keywords: 0332b528-6d94-2603-1e1b-65d4d541f94f, ID3D11View, ID3D11View interface [Direct3D 11], ID3D11View interface [Direct3D 11],described, d3d11/ID3D11View, direct3d11.id3d11view
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
 - ID3D11View
 - d3d11/ID3D11View
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
 - ID3D11View
---

# ID3D11View interface


## -description

A view interface specifies the parts of a resource the pipeline can access during rendering.

## -inheritance

The <b>ID3D11View</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11View</b> also has these types of members:

## -remarks

A view interface is the base interface for all views. There are four types of views; a depth-stencil view, a render-target view, a shader-resource view, and an unordered-access view.

<ul>
<li>To create a render-target view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">ID3D11Device::CreateRenderTargetView</a>.</li>
<li>To create a depth-stencil view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilview">ID3D11Device::CreateDepthStencilView</a>.</li>
<li>To create a shader-resource view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.</li>
<li>To create an unordered-access view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createunorderedaccessview">ID3D11Device::CreateUnorderedAccessView</a>.</li>
</ul>
All resources must be bound to the pipeline before they can be accessed.

<ul>
<li>To bind a render-target view or a depth-stencil view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.</li>
<li>To bind a shader resource, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">ID3D11DeviceContext::VSSetShaderResources</a>.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
