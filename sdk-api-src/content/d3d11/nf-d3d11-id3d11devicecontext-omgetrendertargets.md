---
UID: NF:d3d11.ID3D11DeviceContext.OMGetRenderTargets
title: ID3D11DeviceContext::OMGetRenderTargets (d3d11.h)
description: Get pointers to the resources bound to the output-merger stage. (ID3D11DeviceContext.OMGetRenderTargets)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","OMGetRenderTargets method","ID3D11DeviceContext.OMGetRenderTargets","ID3D11DeviceContext::OMGetRenderTargets","OMGetRenderTargets","OMGetRenderTargets method [Direct3D 11]","OMGetRenderTargets method [Direct3D 11]","ID3D11DeviceContext interface","b914865b-766f-62c4-e7e9-5b7590860668","d3d11/ID3D11DeviceContext::OMGetRenderTargets","direct3d11.id3d11devicecontext_omgetrendertargets"]
old-location: direct3d11\id3d11devicecontext_omgetrendertargets.htm
tech.root: direct3d11
ms.assetid: 27ac656a-0906-43ad-8089-b41639b55ecf
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMGetRenderTargets method, ID3D11DeviceContext.OMGetRenderTargets, ID3D11DeviceContext::OMGetRenderTargets, OMGetRenderTargets, OMGetRenderTargets method [Direct3D 11], OMGetRenderTargets method [Direct3D 11],ID3D11DeviceContext interface, b914865b-766f-62c4-e7e9-5b7590860668, d3d11/ID3D11DeviceContext::OMGetRenderTargets, direct3d11.id3d11devicecontext_omgetrendertargets
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
 - ID3D11DeviceContext::OMGetRenderTargets
 - d3d11/ID3D11DeviceContext::OMGetRenderTargets
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
 - ID3D11DeviceContext.OMGetRenderTargets
---

# ID3D11DeviceContext::OMGetRenderTargets


## -description

Get pointers to the resources bound to the output-merger stage.

## -parameters

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of render targets to retrieve.

### -param ppRenderTargetViews [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>**</b>

Pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>s which represent render target views. Specify <b>NULL</b> for this parameter when retrieval of a render target is not needed.

### -param ppDepthStencilView [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>, which represents a depth-stencil view. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not needed.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
