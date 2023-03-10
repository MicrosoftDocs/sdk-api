---
UID: NF:d3d11_3.ID3D11Device3.CreateRenderTargetView1
title: ID3D11Device3::CreateRenderTargetView1 (d3d11_3.h)
description: Creates a render-target view for accessing resource data. (ID3D11Device3.CreateRenderTargetView1)
helpviewer_keywords: ["CreateRenderTargetView1","CreateRenderTargetView1 method [Direct3D 11]","CreateRenderTargetView1 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","CreateRenderTargetView1 method","ID3D11Device3.CreateRenderTargetView1","ID3D11Device3::CreateRenderTargetView1","d3d11_3/ID3D11Device3::CreateRenderTargetView1","direct3d11.id3d11device3_createrendertargetview1"]
old-location: direct3d11\id3d11device3_createrendertargetview1.htm
tech.root: direct3d11
ms.assetid: 9B85B007-F8B0-43C1-999E-75E5243B7B5A
ms.date: 12/05/2018
ms.keywords: CreateRenderTargetView1, CreateRenderTargetView1 method [Direct3D 11], CreateRenderTargetView1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateRenderTargetView1 method, ID3D11Device3.CreateRenderTargetView1, ID3D11Device3::CreateRenderTargetView1, d3d11_3/ID3D11Device3::CreateRenderTargetView1, direct3d11.id3d11device3_createrendertargetview1
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11Device3::CreateRenderTargetView1
 - d3d11_3/ID3D11Device3::CreateRenderTargetView1
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
 - ID3D11Device3.CreateRenderTargetView1
---

# ID3D11Device3::CreateRenderTargetView1


## -description

Creates a render-target view for accessing resource data.

## -parameters

### -param pResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> that represents a render target. This resource must have been created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a> flag.

### -param pDesc1 [in, optional]

Type: <b>const <a href="/windows/win32/api/d3d11_3/ns-d3d11_3-d3d11_render_target_view_desc1">D3D11_RENDER_TARGET_VIEW_DESC1</a>*</b>

Pointer to a <a href="/windows/win32/api/d3d11_3/ns-d3d11_3-d3d11_render_target_view_desc1">D3D11_RENDER_TARGET_VIEW_DESC1</a> that represents a render-target view description. Set this parameter to <b>NULL</b> to create a view that accesses all of the subresources in mipmap level 0.

### -param ppRTView1 [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11rendertargetview1">ID3D11RenderTargetView1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11rendertargetview1">ID3D11RenderTargetView1</a> interface for the created render-target view. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

A render-target view can be bound to the output-merger stage by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>
