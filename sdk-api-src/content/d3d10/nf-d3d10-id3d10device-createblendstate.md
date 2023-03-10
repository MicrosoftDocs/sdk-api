---
UID: NF:d3d10.ID3D10Device.CreateBlendState
title: ID3D10Device::CreateBlendState (d3d10.h)
description: Create a blend-state object that encapsulates blend state for the output-merger stage. (ID3D10Device.CreateBlendState)
helpviewer_keywords: ["CreateBlendState","CreateBlendState method [Direct3D 10]","CreateBlendState method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateBlendState method","ID3D10Device.CreateBlendState","ID3D10Device::CreateBlendState","c235f4fb-80c3-e358-0ebc-ac3b87230e29","d3d10/ID3D10Device::CreateBlendState","direct3d10.id3d10device_createblendstate"]
old-location: direct3d10\id3d10device_createblendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createblendstate.htm
ms.date: 12/05/2018
ms.keywords: CreateBlendState, CreateBlendState method [Direct3D 10], CreateBlendState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateBlendState method, ID3D10Device.CreateBlendState, ID3D10Device::CreateBlendState, c235f4fb-80c3-e358-0ebc-ac3b87230e29, d3d10/ID3D10Device::CreateBlendState, direct3d10.id3d10device_createblendstate
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
 - ID3D10Device::CreateBlendState
 - d3d10/ID3D10Device::CreateBlendState
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
 - ID3D10Device.CreateBlendState
---

# ID3D10Device::CreateBlendState


## -description

Create a blend-state object that encapsulates blend state for the output-merger stage.

## -parameters

### -param pBlendStateDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">D3D10_BLEND_DESC</a>*</b>

Pointer to a blend-state description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">D3D10_BLEND_DESC</a>).

### -param ppBlendState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>**</b>

Address of a pointer to the blend-state object created (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
