---
UID: NF:d3d11.ID3D11Device.CreateDepthStencilState
title: ID3D11Device::CreateDepthStencilState (d3d11.h)
description: Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage. (ID3D11Device.CreateDepthStencilState)
helpviewer_keywords: ["CreateDepthStencilState","CreateDepthStencilState method [Direct3D 11]","CreateDepthStencilState method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateDepthStencilState method","ID3D11Device.CreateDepthStencilState","ID3D11Device::CreateDepthStencilState","d3d11/ID3D11Device::CreateDepthStencilState","direct3d11.id3d11device_createdepthstencilstate","f09f7b38-23ad-f7a3-93dd-8500c90dc09c"]
old-location: direct3d11\id3d11device_createdepthstencilstate.htm
tech.root: direct3d11
ms.assetid: 7577604c-922c-408c-8eab-2361ebda17df
ms.date: 12/05/2018
ms.keywords: CreateDepthStencilState, CreateDepthStencilState method [Direct3D 11], CreateDepthStencilState method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateDepthStencilState method, ID3D11Device.CreateDepthStencilState, ID3D11Device::CreateDepthStencilState, d3d11/ID3D11Device::CreateDepthStencilState, direct3d11.id3d11device_createdepthstencilstate, f09f7b38-23ad-f7a3-93dd-8500c90dc09c
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
 - ID3D11Device::CreateDepthStencilState
 - d3d11/ID3D11Device::CreateDepthStencilState
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
 - ID3D11Device.CreateDepthStencilState
---

# ID3D11Device::CreateDepthStencilState


## -description

Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage.

## -parameters

### -param pDepthStencilDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>*</b>

Pointer to a depth-stencil state description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>).

### -param ppDepthStencilState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>**</b>

Address of a pointer to the depth-stencil state object created (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

4096 unique depth-stencil state objects can be created on a device at a time.

If an application attempts to create a depth-stencil-state interface with the same state as an existing interface, the same interface will be returned and the total number of unique depth-stencil state objects will stay the same.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
