---
UID: NF:d3d10.ID3D10Device.CreateRasterizerState
title: ID3D10Device::CreateRasterizerState (d3d10.h)
description: Create a rasterizer state object that tells the rasterizer stage how to behave. (ID3D10Device.CreateRasterizerState)
helpviewer_keywords: ["CreateRasterizerState","CreateRasterizerState method [Direct3D 10]","CreateRasterizerState method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateRasterizerState method","ID3D10Device.CreateRasterizerState","ID3D10Device::CreateRasterizerState","b5877d5f-3976-076e-eb6a-ddf73c6f4995","d3d10/ID3D10Device::CreateRasterizerState","direct3d10.id3d10device_createrasterizerstate"]
old-location: direct3d10\id3d10device_createrasterizerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createrasterizerstate.htm
ms.date: 12/05/2018
ms.keywords: CreateRasterizerState, CreateRasterizerState method [Direct3D 10], CreateRasterizerState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateRasterizerState method, ID3D10Device.CreateRasterizerState, ID3D10Device::CreateRasterizerState, b5877d5f-3976-076e-eb6a-ddf73c6f4995, d3d10/ID3D10Device::CreateRasterizerState, direct3d10.id3d10device_createrasterizerstate
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
 - ID3D10Device::CreateRasterizerState
 - d3d10/ID3D10Device::CreateRasterizerState
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
 - ID3D10Device.CreateRasterizerState
---

# ID3D10Device::CreateRasterizerState


## -description

Create a rasterizer state object that tells the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> how to behave.

## -parameters

### -param pRasterizerDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>*</b>

Pointer to a rasterizer state description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>).

### -param ppRasterizerState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>**</b>

Address of a pointer to the rasterizer state object created (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

4096 unique rasterizer state objects can be created on a device at a time.

If an application attempts to create a rasterizer state with the same description as an already existing rasterizer state, then the same interface with an incremented reference count will be returned and the total number of unique rasterizer state objects will stay the same.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
