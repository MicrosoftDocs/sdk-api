---
UID: NF:d3d11.ID3D11DeviceContext.RSGetState
title: ID3D11DeviceContext::RSGetState (d3d11.h)
description: Get the rasterizer state from the rasterizer stage of the pipeline. (ID3D11DeviceContext.RSGetState)
helpviewer_keywords: ["7de5d766-760e-6053-6c62-f66f824404ea","ID3D11DeviceContext interface [Direct3D 11]","RSGetState method","ID3D11DeviceContext.RSGetState","ID3D11DeviceContext::RSGetState","RSGetState","RSGetState method [Direct3D 11]","RSGetState method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::RSGetState","direct3d11.id3d11devicecontext_rsgetstate"]
old-location: direct3d11\id3d11devicecontext_rsgetstate.htm
tech.root: direct3d11
ms.assetid: bd1ade36-e57c-4776-ab59-ba8b59276369
ms.date: 12/05/2018
ms.keywords: 7de5d766-760e-6053-6c62-f66f824404ea, ID3D11DeviceContext interface [Direct3D 11],RSGetState method, ID3D11DeviceContext.RSGetState, ID3D11DeviceContext::RSGetState, RSGetState, RSGetState method [Direct3D 11], RSGetState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSGetState, direct3d11.id3d11devicecontext_rsgetstate
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
 - ID3D11DeviceContext::RSGetState
 - d3d11/ID3D11DeviceContext::RSGetState
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
 - ID3D11DeviceContext.RSGetState
---

# ID3D11DeviceContext::RSGetState


## -description

Get the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">rasterizer state</a> from the rasterizer stage of the pipeline.

## -parameters

### -param ppRasterizerState [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>**</b>

Address of a pointer to a rasterizer-state interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>) to fill with information from the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
