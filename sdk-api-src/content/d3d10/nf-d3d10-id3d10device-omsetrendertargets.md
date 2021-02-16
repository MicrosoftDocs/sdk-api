---
UID: NF:d3d10.ID3D10Device.OMSetRenderTargets
title: ID3D10Device::OMSetRenderTargets (d3d10.h)
description: Bind one or more render targets and the depth-stencil buffer to the output-merger stage.
helpviewer_keywords: ["1a066759-273f-afca-4fed-6d836735ff9f","ID3D10Device interface [Direct3D 10]","OMSetRenderTargets method","ID3D10Device.OMSetRenderTargets","ID3D10Device::OMSetRenderTargets","OMSetRenderTargets","OMSetRenderTargets method [Direct3D 10]","OMSetRenderTargets method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::OMSetRenderTargets","direct3d10.id3d10device_omsetrendertargets"]
old-location: direct3d10\id3d10device_omsetrendertargets.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omsetrendertargets.htm
ms.date: 12/05/2018
ms.keywords: 1a066759-273f-afca-4fed-6d836735ff9f, ID3D10Device interface [Direct3D 10],OMSetRenderTargets method, ID3D10Device.OMSetRenderTargets, ID3D10Device::OMSetRenderTargets, OMSetRenderTargets, OMSetRenderTargets method [Direct3D 10], OMSetRenderTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMSetRenderTargets, direct3d10.id3d10device_omsetrendertargets
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
 - ID3D10Device::OMSetRenderTargets
 - d3d10/ID3D10Device::OMSetRenderTargets
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
 - ID3D10Device.OMSetRenderTargets
---

# ID3D10Device::OMSetRenderTargets


## -description

Bind one or more render targets and the depth-stencil buffer to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a>.

## -parameters

### -param NumViews [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of render targets to bind.

### -param ppRenderTargetViews [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>*</b>

Pointer to an array of render targets (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>) to bind to the device. If this parameter is <b>NULL</b>, no render targets are bound. See Remarks.

### -param pDepthStencilView [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>*</b>

Pointer to a depth-stencil view (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>) to bind to the device. If this parameter is <b>NULL</b>, the depth-stencil state is not bound.

## -remarks

A call to <b>OMSetRenderTargets</b> overrides all bounded render targets and the depth stencil target regardless of the number of render targets in <i>ppRenderTargetViews</i>.

The maximum number of render targets a device can have active at any given time is set by a #define in D3D10.h called D3D10_SIMULTANEOUS_RENDER_TARGET_COUNT. It is invalid to try to set the same <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> to multiple render target slots.

If any subresources are also currently bound for reading or writing (perhaps in a different part of the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a>), those bind points will be <b>NULL</b>'ed out to prevent the same subresource from being read and written simultaneously in a single rendering operation.

The method will not hold references to the interfaces passed in. For that reason, applications should be careful not to release interfaces currently in use by the device.

See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Binding Resources and Pipeline stages</a> for more information on binding resources.

The pixel shader must be able to simultaneously render to at least eight separate render targets. All of these render targets must access the same type of resource: <a href="/windows/desktop/direct3dhlsl/sm5-object-buffer">Buffer</a>, <a href="/windows/desktop/direct3dhlsl/sm5-object-texture1d">Texture1D</a>, <a href="/windows/desktop/direct3dhlsl/sm5-object-texture1darray">Texture1DArray</a>, <a href="/windows/desktop/direct3dhlsl/sm5-object-texture2d">Texture2D</a>, <a href="/windows/desktop/direct3dhlsl/sm5-object-texture2darray">Texture2DArray</a>, <a href="/windows/desktop/direct3dhlsl/sm5-object-texture3d">Texture3D</a>, or <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type">TextureCube</a>. All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for *Array types). If render targets use multisample anti-aliasing, all bound render targets and depth buffer must be the same form of multisample resource (that is, the sample counts must be the same). Each render target can have a different data format. These render target formats are not required to have identical bit-per-element counts.

Any combination of the eight slots for render targets can have a render target set or not set.

The same resource view cannot be bound to multiple render target slots simultaneously. However, you can set multiple non-overlapping resource views of a single resource as simultaneous multiple render targets.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>