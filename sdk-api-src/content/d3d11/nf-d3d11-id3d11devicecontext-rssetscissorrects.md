---
UID: NF:d3d11.ID3D11DeviceContext.RSSetScissorRects
title: ID3D11DeviceContext::RSSetScissorRects (d3d11.h)
description: Bind an array of scissor rectangles to the rasterizer stage. (ID3D11DeviceContext.RSSetScissorRects)
helpviewer_keywords: ["28026545-0d38-beff-91cf-a929caef1657","ID3D11DeviceContext interface [Direct3D 11]","RSSetScissorRects method","ID3D11DeviceContext.RSSetScissorRects","ID3D11DeviceContext::RSSetScissorRects","RSSetScissorRects","RSSetScissorRects method [Direct3D 11]","RSSetScissorRects method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::RSSetScissorRects","direct3d11.id3d11devicecontext_rssetscissorrects"]
old-location: direct3d11\id3d11devicecontext_rssetscissorrects.htm
tech.root: direct3d11
ms.assetid: 80bee89d-1743-475c-a284-8137cfacdac2
ms.date: 12/05/2018
ms.keywords: 28026545-0d38-beff-91cf-a929caef1657, ID3D11DeviceContext interface [Direct3D 11],RSSetScissorRects method, ID3D11DeviceContext.RSSetScissorRects, ID3D11DeviceContext::RSSetScissorRects, RSSetScissorRects, RSSetScissorRects method [Direct3D 11], RSSetScissorRects method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSSetScissorRects, direct3d11.id3d11devicecontext_rssetscissorrects
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
 - ID3D11DeviceContext::RSSetScissorRects
 - d3d11/ID3D11DeviceContext::RSSetScissorRects
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
 - ID3D11DeviceContext.RSSetScissorRects
---

# ID3D11DeviceContext::RSSetScissorRects


## -description

Bind an array of scissor rectangles to the rasterizer stage.

## -parameters

### -param NumRects [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of scissor rectangles to bind.

### -param pRects [in, optional]

Type: <b>const <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a>*</b>

An array of scissor rectangles (see <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a>).

## -remarks

All scissor rects must be set atomically as one operation. Any scissor rects not defined by the call are disabled.

The scissor rectangles will only be used if ScissorEnable is set to true in the rasterizer state (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>).
        

Which scissor rectangle to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see shader semantic syntax). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first scissor rectangle in the array.

Each scissor rectangle in the array corresponds to a viewport in an array of viewports (see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetviewports">ID3D11DeviceContext::RSSetViewports</a>).
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
