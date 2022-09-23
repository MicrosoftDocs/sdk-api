---
UID: NF:d3d11.ID3D11DeviceContext.RSGetScissorRects
title: ID3D11DeviceContext::RSGetScissorRects (d3d11.h)
description: Get the array of scissor rectangles bound to the rasterizer stage. (ID3D11DeviceContext.RSGetScissorRects)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","RSGetScissorRects method","ID3D11DeviceContext.RSGetScissorRects","ID3D11DeviceContext::RSGetScissorRects","RSGetScissorRects","RSGetScissorRects method [Direct3D 11]","RSGetScissorRects method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::RSGetScissorRects","direct3d11.id3d11devicecontext_rsgetscissorrects","e30c7e76-70dc-8be0-b80a-ea7965268531"]
old-location: direct3d11\id3d11devicecontext_rsgetscissorrects.htm
tech.root: direct3d11
ms.assetid: 83676c65-e5d8-44c9-bc0d-ebe9850cb382
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],RSGetScissorRects method, ID3D11DeviceContext.RSGetScissorRects, ID3D11DeviceContext::RSGetScissorRects, RSGetScissorRects, RSGetScissorRects method [Direct3D 11], RSGetScissorRects method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSGetScissorRects, direct3d11.id3d11devicecontext_rsgetscissorrects, e30c7e76-70dc-8be0-b80a-ea7965268531
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
 - ID3D11DeviceContext::RSGetScissorRects
 - d3d11/ID3D11DeviceContext::RSGetScissorRects
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
 - ID3D11DeviceContext.RSGetScissorRects
---

# ID3D11DeviceContext::RSGetScissorRects


## -description

Get the array of scissor rectangles bound to the rasterizer stage.

## -parameters

### -param pNumRects [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

The number of scissor rectangles (ranges between 0 and D3D11_VIEWPORT_AND_SCISSORRECT_OBJECT_COUNT_PER_PIPELINE) bound; set <i>pRects</i> to <b>NULL</b> to use <i>pNumRects</i> to see how many rectangles would be returned.

### -param pRects [out, optional]

Type: <b><a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a>*</b>

An array of scissor rectangles (see <a href="/windows/desktop/direct3d11/d3d11-rect">D3D11_RECT</a>). If NumRects is greater than the number of scissor rects currently bound, then unused members of the array will contain 0.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
