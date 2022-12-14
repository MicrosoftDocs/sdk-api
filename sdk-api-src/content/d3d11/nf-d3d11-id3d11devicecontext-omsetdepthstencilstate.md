---
UID: NF:d3d11.ID3D11DeviceContext.OMSetDepthStencilState
title: ID3D11DeviceContext::OMSetDepthStencilState (d3d11.h)
description: Sets the depth-stencil state of the output-merger stage. (ID3D11DeviceContext.OMSetDepthStencilState)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","OMSetDepthStencilState method","ID3D11DeviceContext.OMSetDepthStencilState","ID3D11DeviceContext::OMSetDepthStencilState","OMSetDepthStencilState","OMSetDepthStencilState method [Direct3D 11]","OMSetDepthStencilState method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMSetDepthStencilState","direct3d11.id3d11devicecontext_omsetdepthstencilstate","faf5401a-abab-bc40-9854-cf64f6ca05eb"]
old-location: direct3d11\id3d11devicecontext_omsetdepthstencilstate.htm
tech.root: direct3d11
ms.assetid: cd5642c4-8bbe-4b5d-9f04-87de82ee9601
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMSetDepthStencilState method, ID3D11DeviceContext.OMSetDepthStencilState, ID3D11DeviceContext::OMSetDepthStencilState, OMSetDepthStencilState, OMSetDepthStencilState method [Direct3D 11], OMSetDepthStencilState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetDepthStencilState, direct3d11.id3d11devicecontext_omsetdepthstencilstate, faf5401a-abab-bc40-9854-cf64f6ca05eb
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
 - ID3D11DeviceContext::OMSetDepthStencilState
 - d3d11/ID3D11DeviceContext::OMSetDepthStencilState
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
 - ID3D11DeviceContext.OMSetDepthStencilState
---

# ID3D11DeviceContext::OMSetDepthStencilState


## -description

Sets the depth-stencil state of the output-merger stage.

## -parameters

### -param pDepthStencilState [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>*</b>

Pointer to a depth-stencil state interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>) to bind to the device. Set this to <b>NULL</b> to use the default state listed in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>.

### -param StencilRef [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reference value to perform against when doing a depth-stencil test. See remarks.

## -remarks

To create a depth-stencil state interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilstate">ID3D11Device::CreateDepthStencilState</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
