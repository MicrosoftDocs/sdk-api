---
UID: NF:d3d11.ID3D11Device.CreateRasterizerState
title: ID3D11Device::CreateRasterizerState (d3d11.h)
description: Create a rasterizer state object that tells the rasterizer stage how to behave. (ID3D11Device.CreateRasterizerState)
helpviewer_keywords: ["89e8a772-b143-38e2-89a4-4b72b0a4b1c5","CreateRasterizerState","CreateRasterizerState method [Direct3D 11]","CreateRasterizerState method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateRasterizerState method","ID3D11Device.CreateRasterizerState","ID3D11Device::CreateRasterizerState","d3d11/ID3D11Device::CreateRasterizerState","direct3d11.id3d11device_createrasterizerstate"]
old-location: direct3d11\id3d11device_createrasterizerstate.htm
tech.root: direct3d11
ms.assetid: b49a8dbb-2280-4d5d-ae65-58cde2e9ed10
ms.date: 12/05/2018
ms.keywords: 89e8a772-b143-38e2-89a4-4b72b0a4b1c5, CreateRasterizerState, CreateRasterizerState method [Direct3D 11], CreateRasterizerState method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateRasterizerState method, ID3D11Device.CreateRasterizerState, ID3D11Device::CreateRasterizerState, d3d11/ID3D11Device::CreateRasterizerState, direct3d11.id3d11device_createrasterizerstate
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
 - ID3D11Device::CreateRasterizerState
 - d3d11/ID3D11Device::CreateRasterizerState
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
 - ID3D11Device.CreateRasterizerState
---

# ID3D11Device::CreateRasterizerState


## -description

Create a rasterizer state object that tells the rasterizer stage how to behave.

## -parameters

### -param pRasterizerDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>*</b>

Pointer to a rasterizer state description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>).

### -param ppRasterizerState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>**</b>

Address of a pointer to the rasterizer state object created (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the compute shader.  See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -remarks

4096 unique rasterizer state objects can be created on a device at a time.

If an application attempts to create a rasterizer-state interface with the same state as an existing interface, the same interface will be returned and the total number of unique rasterizer state objects will stay the same.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
