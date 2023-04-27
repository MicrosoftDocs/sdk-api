---
UID: NF:d3d11.ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews
title: ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews (d3d11.h)
description: Get pointers to the resources bound to the output-merger stage. (ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews)
helpviewer_keywords: ["84c4c039-405e-ee3a-22d0-80eb7078ffe8","ID3D11DeviceContext interface [Direct3D 11]","OMGetRenderTargetsAndUnorderedAccessViews method","ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews","ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews","OMGetRenderTargetsAndUnorderedAccessViews","OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11]","OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews","direct3d11.id3d11devicecontext_omgetrendertargetsandunorderedaccessviews"]
old-location: direct3d11\id3d11devicecontext_omgetrendertargetsandunorderedaccessviews.htm
tech.root: direct3d11
ms.assetid: 5baaedea-5db4-4a25-adfc-2ac9cf48ad6d
ms.date: 12/05/2018
ms.keywords: 84c4c039-405e-ee3a-22d0-80eb7078ffe8, ID3D11DeviceContext interface [Direct3D 11],OMGetRenderTargetsAndUnorderedAccessViews method, ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews, ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews, OMGetRenderTargetsAndUnorderedAccessViews, OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11], OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews, direct3d11.id3d11devicecontext_omgetrendertargetsandunorderedaccessviews
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
 - ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews
 - d3d11/ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews
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
 - ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews
---

# ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews


## -description

Get pointers to the resources bound to the output-merger stage.

## -parameters

### -param NumRTVs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of render-target views to retrieve.

### -param ppRenderTargetViews [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>**</b>

Pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>s, which represent render-target views. Specify <b>NULL</b> for this parameter when retrieval of render-target views is not required.

### -param ppDepthStencilView [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>, which represents a depth-stencil view. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not required.

### -param UAVStartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into a zero-based array to begin retrieving unordered-access views (ranges from 0 to D3D11_PS_CS_UAV_REGISTER_COUNT - 1).
            For pixel shaders <i>UAVStartSlot</i> should be equal to the number of render-target views that are bound.

### -param NumUAVs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of unordered-access views to return in <i>ppUnorderedAccessViews</i>. This number ranges from 0 to D3D11_PS_CS_UAV_REGISTER_COUNT - <i>UAVStartSlot</i>.

### -param ppUnorderedAccessViews [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>**</b>

Pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>s, which represent unordered-access views that are retrieved. Specify <b>NULL</b> for this parameter when retrieval of unordered-access views is not required.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
