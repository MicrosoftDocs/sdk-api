---
UID: NF:d3d10.ID3D10Device.CreateDepthStencilView
title: ID3D10Device::CreateDepthStencilView (d3d10.h)
description: Create a depth-stencil view for accessing resource data. (ID3D10Device.CreateDepthStencilView)
helpviewer_keywords: ["CreateDepthStencilView","CreateDepthStencilView method [Direct3D 10]","CreateDepthStencilView method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateDepthStencilView method","ID3D10Device.CreateDepthStencilView","ID3D10Device::CreateDepthStencilView","d3d10/ID3D10Device::CreateDepthStencilView","direct3d10.id3d10device_createdepthstencilview","f7b0585b-710f-b4d1-e65f-c30b57116c09"]
old-location: direct3d10\id3d10device_createdepthstencilview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createdepthstencilview.htm
ms.date: 12/05/2018
ms.keywords: CreateDepthStencilView, CreateDepthStencilView method [Direct3D 10], CreateDepthStencilView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateDepthStencilView method, ID3D10Device.CreateDepthStencilView, ID3D10Device::CreateDepthStencilView, d3d10/ID3D10Device::CreateDepthStencilView, direct3d10.id3d10device_createdepthstencilview, f7b0585b-710f-b4d1-e65f-c30b57116c09
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
 - ID3D10Device::CreateDepthStencilView
 - d3d10/ID3D10Device::CreateDepthStencilView
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
 - ID3D10Device.CreateDepthStencilView
---

# ID3D10Device::CreateDepthStencilView


## -description

Create a depth-stencil <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing resource data.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

Pointer to the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resource</a> that will serve as the depth-stencil surface. This resource must have been created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_DEPTH_STENCIL</a> flag.

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_view_desc">D3D10_DEPTH_STENCIL_VIEW_DESC</a>*</b>

Pointer to a depth-stencil-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_view_desc">D3D10_DEPTH_STENCIL_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).

### -param ppDepthStencilView [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A depth-stencil view can be bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">ID3D10Device::OMSetRenderTargets</a>.

For more background information, see the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-depth-stencil">programming guide page</a> about depth stencils.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
