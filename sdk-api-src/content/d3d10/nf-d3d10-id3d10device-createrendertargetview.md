---
UID: NF:d3d10.ID3D10Device.CreateRenderTargetView
title: ID3D10Device::CreateRenderTargetView (d3d10.h)
description: Create a render-target view for accessing resource data.
helpviewer_keywords: ["080acf2e-83e1-3be3-60d6-8385a6585f49","CreateRenderTargetView","CreateRenderTargetView method [Direct3D 10]","CreateRenderTargetView method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateRenderTargetView method","ID3D10Device.CreateRenderTargetView","ID3D10Device::CreateRenderTargetView","d3d10/ID3D10Device::CreateRenderTargetView","direct3d10.id3d10device_createrendertargetview"]
old-location: direct3d10\id3d10device_createrendertargetview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createrendertargetview.htm
ms.date: 12/05/2018
ms.keywords: 080acf2e-83e1-3be3-60d6-8385a6585f49, CreateRenderTargetView, CreateRenderTargetView method [Direct3D 10], CreateRenderTargetView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateRenderTargetView method, ID3D10Device.CreateRenderTargetView, ID3D10Device::CreateRenderTargetView, d3d10/ID3D10Device::CreateRenderTargetView, direct3d10.id3d10device_createrendertargetview
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
 - ID3D10Device::CreateRenderTargetView
 - d3d10/ID3D10Device::CreateRenderTargetView
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
 - ID3D10Device.CreateRenderTargetView
---

# ID3D10Device::CreateRenderTargetView


## -description

Create a render-target <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> for accessing resource data.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

Pointer to the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resource</a> that will serve as the render target. This resource must have been created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_RENDER_TARGET</a> flag.

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>*</b>

Pointer to a render-target-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_render_target_view_desc">D3D10_RENDER_TARGET_VIEW_DESC</a>). Set this parameter to <b>NULL</b> to create a view that accesses mipmap level 0 of the entire resource (using the format the resource was created with).

### -param ppRTView [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A rendertarget view can be bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output merger stage</a> by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetrendertargets">ID3D10Device::OMSetRenderTargets</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>