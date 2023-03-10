---
UID: NF:d3d11.ID3D11Device.CreateBlendState
title: ID3D11Device::CreateBlendState (d3d11.h)
description: Create a blend-state object that encapsulates blend state for the output-merger stage. (ID3D11Device.CreateBlendState)
helpviewer_keywords: ["3e6800b8-cd67-743c-c74d-b23a9a29daea","CreateBlendState","CreateBlendState method [Direct3D 11]","CreateBlendState method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateBlendState method","ID3D11Device.CreateBlendState","ID3D11Device::CreateBlendState","d3d11/ID3D11Device::CreateBlendState","direct3d11.id3d11device_createblendstate"]
old-location: direct3d11\id3d11device_createblendstate.htm
tech.root: direct3d11
ms.assetid: 05b27d72-6ae5-4bab-8906-2d1373ea8d4c
ms.date: 12/05/2018
ms.keywords: 3e6800b8-cd67-743c-c74d-b23a9a29daea, CreateBlendState, CreateBlendState method [Direct3D 11], CreateBlendState method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateBlendState method, ID3D11Device.CreateBlendState, ID3D11Device::CreateBlendState, d3d11/ID3D11Device::CreateBlendState, direct3d11.id3d11device_createblendstate
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
 - ID3D11Device::CreateBlendState
 - d3d11/ID3D11Device::CreateBlendState
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
 - ID3D11Device.CreateBlendState
---

# ID3D11Device::CreateBlendState


## -description

Create a blend-state object that encapsulates blend state for the output-merger stage.

## -parameters

### -param pBlendStateDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">D3D11_BLEND_DESC</a>*</b>

Pointer to a blend-state description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">D3D11_BLEND_DESC</a>).

### -param ppBlendState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>**</b>

Address of a pointer to the blend-state object created (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the blend-state object.
              See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -remarks

An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object
          has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
