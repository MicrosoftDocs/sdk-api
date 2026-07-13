---
UID: NF:d3d10.ID3D10Device.RSSetScissorRects
title: ID3D10Device::RSSetScissorRects (d3d10.h)
description: Bind an array of scissor rectangles to the rasterizer stage. (ID3D10Device.RSSetScissorRects)
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","RSSetScissorRects method","ID3D10Device.RSSetScissorRects","ID3D10Device::RSSetScissorRects","RSSetScissorRects","RSSetScissorRects method [Direct3D 10]","RSSetScissorRects method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::RSSetScissorRects","direct3d10.id3d10device_rssetscissorrects","ff11533a-fe9e-059e-c169-7e6f3c873b2d"]
old-location: direct3d10\id3d10device_rssetscissorrects.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetscissorrects.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSSetScissorRects method, ID3D10Device.RSSetScissorRects, ID3D10Device::RSSetScissorRects, RSSetScissorRects, RSSetScissorRects method [Direct3D 10], RSSetScissorRects method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSSetScissorRects, direct3d10.id3d10device_rssetscissorrects, ff11533a-fe9e-059e-c169-7e6f3c873b2d
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
 - ID3D10Device::RSSetScissorRects
 - d3d10/ID3D10Device::RSSetScissorRects
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
 - ID3D10Device.RSSetScissorRects
---

# ID3D10Device::RSSetScissorRects


## -description

Bind an array of <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">scissor rectangles</a> to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>.

## -parameters

### -param NumRects [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of scissor rectangles to bind.

### -param pRects [in]

Type: <b>const <a href="/windows/desktop/direct3d10/d3d10-rect">D3D10_RECT</a>*</b>

An array of scissor rectangles (see <a href="/windows/desktop/direct3d10/d3d10-rect">D3D10_RECT</a>).

## -remarks

The scissor rectangles will only be used if ScissorEnable is set to true in the rasterizer state (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>).

Which scissor rectangle to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">shader semantic syntax</a>). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first scissor rectangle in the array.

Each scissor rectangle in the array corresponds to a viewport in an array of viewports (see <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-rssetviewports">ID3D10Device::RSSetViewports</a>).

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
