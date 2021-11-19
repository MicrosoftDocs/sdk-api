---
UID: NF:d3d11.ID3D11DeviceContext.OMSetRenderTargets
title: ID3D11DeviceContext::OMSetRenderTargets (d3d11.h)
description: Bind one or more render targets atomically and the depth-stencil buffer to the output-merger stage.
helpviewer_keywords: ["57e16a81-6543-5ac7-d96c-aac3ca8504f8","ID3D11DeviceContext interface [Direct3D 11]","OMSetRenderTargets method","ID3D11DeviceContext.OMSetRenderTargets","ID3D11DeviceContext::OMSetRenderTargets","OMSetRenderTargets","OMSetRenderTargets method [Direct3D 11]","OMSetRenderTargets method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMSetRenderTargets","direct3d11.id3d11devicecontext_omsetrendertargets"]
old-location: direct3d11\id3d11devicecontext_omsetrendertargets.htm
tech.root: direct3d11
ms.assetid: 65514812-7433-4c13-a6cb-53980dacdf65
ms.date: 12/05/2018
ms.keywords: 57e16a81-6543-5ac7-d96c-aac3ca8504f8, ID3D11DeviceContext interface [Direct3D 11],OMSetRenderTargets method, ID3D11DeviceContext.OMSetRenderTargets, ID3D11DeviceContext::OMSetRenderTargets, OMSetRenderTargets, OMSetRenderTargets method [Direct3D 11], OMSetRenderTargets method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetRenderTargets, direct3d11.id3d11devicecontext_omsetrendertargets
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
 - ID3D11DeviceContext::OMSetRenderTargets
 - d3d11/ID3D11DeviceContext::OMSetRenderTargets
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
 - ID3D11DeviceContext.OMSetRenderTargets
---

## -description

Bind one or more render targets atomically and the depth-stencil buffer to the <a href="/windows/win32/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

## -parameters

### -param NumViews [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

Number of render targets to bind (ranges between 0 and <b>D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT</b>). If this parameter is nonzero, the number of entries in the array to which <i>ppRenderTargetViews</i> points must equal the number in this parameter.

### -param ppRenderTargetViews [in, optional]

Type: <b><a href="/windows/win32/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>*</b>

Pointer to an array of <a href="/windows/win32/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a> that represent the render targets to bind to the device. 
        If this parameter is <b>NULL</b> and <i>NumViews</i> is 0, no render targets are bound.

### -param pDepthStencilView [in, optional]

Type: <b><a href="/windows/win32/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>*</b>

Pointer to a <a href="/windows/win32/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a> that represents the depth-stencil view to bind to the device. 
        If this parameter is <b>NULL</b>, the depth-stencil view is not bound.

## -remarks

The maximum number of active render targets a device can have active at any given time is set by a #define in D3D11.h called 
      <b>D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT</b>. It is invalid to try to set the same subresource to multiple render target slots. 
      Any render targets not defined by this call are set to <b>NULL</b>.

If any subresources are also currently bound for reading in a different stage or writing (perhaps in a different part of the pipeline), 
      those bind points will be set to <b>NULL</b>, in order to prevent the same subresource from being read and written simultaneously in a single rendering operation.

The method will hold a reference to the interfaces passed in.
        This differs from the device state behavior in Direct3D 10.

If the render-target views were created from an array resource type, all of the render-target views must have the same array size.  
      This restriction also applies to the depth-stencil view, its array size must match that of the render-target views being bound.

The pixel shader must be able to simultaneously render to at least eight separate render targets. All of these render targets must access the same type of resource: <a href="/windows/win32/direct3dhlsl/sm5-object-buffer">Buffer</a>, <a href="/windows/win32/direct3dhlsl/sm5-object-texture1d">Texture1D</a>, <a href="/windows/win32/direct3dhlsl/sm5-object-texture1darray">Texture1DArray</a>, <a href="/windows/win32/direct3dhlsl/sm5-object-texture2d">Texture2D</a>, <a href="/windows/win32/direct3dhlsl/sm5-object-texture2darray">Texture2DArray</a>, <a href="/windows/win32/direct3dhlsl/sm5-object-texture3d">Texture3D</a>, or <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-type">TextureCube</a>. All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for *Array types). If render targets use multisample anti-aliasing, all bound render targets and depth buffer must be the same form of multisample resource (that is, the sample counts must be the same). Each render target can have a different data format. These render target formats are not required to have identical bit-per-element counts.

Any combination of the eight slots for render targets can have a render target set or not set.

The same resource view cannot be bound to multiple render target slots simultaneously. However, you can set multiple non-overlapping resource views of a single resource as simultaneous multiple render targets.

Note that unlike some other resource methods in Direct3D, all currently bound render targets will be unbound by calling `OMSetRenderTargets(0, nullptr, nullptr);`.

## -see-also

<a href="/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
