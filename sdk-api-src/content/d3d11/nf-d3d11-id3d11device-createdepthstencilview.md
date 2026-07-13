---
UID: NF:d3d11.ID3D11Device.CreateDepthStencilView
title: ID3D11Device::CreateDepthStencilView (d3d11.h)
description: Create a depth-stencil view for accessing resource data. (ID3D11Device.CreateDepthStencilView)
helpviewer_keywords: ["CreateDepthStencilView","CreateDepthStencilView method [Direct3D 11]","CreateDepthStencilView method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateDepthStencilView method","ID3D11Device.CreateDepthStencilView","ID3D11Device::CreateDepthStencilView","d3d11/ID3D11Device::CreateDepthStencilView","direct3d11.id3d11device_createdepthstencilview","e1e786e8-1374-b092-ac91-06c2482f6166"]
old-location: direct3d11\id3d11device_createdepthstencilview.htm
tech.root: direct3d11
ms.assetid: b3e899eb-3df6-421f-bdc8-98d7c7acbe62
ms.date: 12/05/2018
ms.keywords: CreateDepthStencilView, CreateDepthStencilView method [Direct3D 11], CreateDepthStencilView method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateDepthStencilView method, ID3D11Device.CreateDepthStencilView, ID3D11Device::CreateDepthStencilView, d3d11/ID3D11Device::CreateDepthStencilView, direct3d11.id3d11device_createdepthstencilview, e1e786e8-1374-b092-ac91-06c2482f6166
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreateDepthStencilView
 - d3d11/ID3D11Device::CreateDepthStencilView
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
 - ID3D11Device.CreateDepthStencilView
---

# ID3D11Device::CreateDepthStencilView


## -description

Create a depth-stencil view for accessing resource data.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

Pointer to the resource that will serve as the depth-stencil surface. This resource must have been created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_DEPTH_STENCIL</a> flag.

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a>*</b>

Pointer to a depth-stencil-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).

### -param ppDepthStencilView [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

A depth-stencil view can be bound to the output-merger stage by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
