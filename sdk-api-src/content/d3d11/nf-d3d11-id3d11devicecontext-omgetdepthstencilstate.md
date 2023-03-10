---
UID: NF:d3d11.ID3D11DeviceContext.OMGetDepthStencilState
title: ID3D11DeviceContext::OMGetDepthStencilState (d3d11.h)
description: Gets the depth-stencil state of the output-merger stage. (ID3D11DeviceContext.OMGetDepthStencilState)
helpviewer_keywords: ["46d0ab14-fdda-10ce-1e1a-4e551e1deeb3","ID3D11DeviceContext interface [Direct3D 11]","OMGetDepthStencilState method","ID3D11DeviceContext.OMGetDepthStencilState","ID3D11DeviceContext::OMGetDepthStencilState","OMGetDepthStencilState","OMGetDepthStencilState method [Direct3D 11]","OMGetDepthStencilState method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMGetDepthStencilState","direct3d11.id3d11devicecontext_omgetdepthstencilstate"]
old-location: direct3d11\id3d11devicecontext_omgetdepthstencilstate.htm
tech.root: direct3d11
ms.assetid: d5ea53a8-62c9-46c9-96ed-8c9977d916b2
ms.date: 12/05/2018
ms.keywords: 46d0ab14-fdda-10ce-1e1a-4e551e1deeb3, ID3D11DeviceContext interface [Direct3D 11],OMGetDepthStencilState method, ID3D11DeviceContext.OMGetDepthStencilState, ID3D11DeviceContext::OMGetDepthStencilState, OMGetDepthStencilState, OMGetDepthStencilState method [Direct3D 11], OMGetDepthStencilState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetDepthStencilState, direct3d11.id3d11devicecontext_omgetdepthstencilstate
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
 - ID3D11DeviceContext::OMGetDepthStencilState
 - d3d11/ID3D11DeviceContext::OMGetDepthStencilState
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
 - ID3D11DeviceContext.OMGetDepthStencilState
---

# ID3D11DeviceContext::OMGetDepthStencilState


## -description

Gets the depth-stencil state of the output-merger stage.

## -parameters

### -param ppDepthStencilState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>**</b>

Address of a pointer to a depth-stencil state interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>) to be filled with information from the device.

### -param pStencilRef [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to the stencil reference value used in the depth-stencil test.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
