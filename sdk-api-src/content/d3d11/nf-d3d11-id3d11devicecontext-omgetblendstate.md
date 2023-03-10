---
UID: NF:d3d11.ID3D11DeviceContext.OMGetBlendState
title: ID3D11DeviceContext::OMGetBlendState (d3d11.h)
description: Get the blend state of the output-merger stage. (ID3D11DeviceContext.OMGetBlendState)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","OMGetBlendState method","ID3D11DeviceContext.OMGetBlendState","ID3D11DeviceContext::OMGetBlendState","OMGetBlendState","OMGetBlendState method [Direct3D 11]","OMGetBlendState method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMGetBlendState","db30eb26-ca10-d827-172b-7c7a6fe1ff83","direct3d11.id3d11devicecontext_omgetblendstate"]
old-location: direct3d11\id3d11devicecontext_omgetblendstate.htm
tech.root: direct3d11
ms.assetid: 871429b4-8f4a-43bb-ae55-3b07f8d00f68
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMGetBlendState method, ID3D11DeviceContext.OMGetBlendState, ID3D11DeviceContext::OMGetBlendState, OMGetBlendState, OMGetBlendState method [Direct3D 11], OMGetBlendState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetBlendState, db30eb26-ca10-d827-172b-7c7a6fe1ff83, direct3d11.id3d11devicecontext_omgetblendstate
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
 - ID3D11DeviceContext::OMGetBlendState
 - d3d11/ID3D11DeviceContext::OMGetBlendState
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
 - ID3D11DeviceContext.OMGetBlendState
---

# ID3D11DeviceContext::OMGetBlendState


## -description

Get the blend state of the output-merger stage.

## -parameters

### -param ppBlendState [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>**</b>

Address of a pointer to a blend-state interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>).

### -param BlendFactor [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a>[4]</b>

Array of blend factors, one for each RGBA component.

### -param pSampleMask [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">sample mask</a>.

## -remarks

The reference count of the returned interface will be incremented by one when the blend state is retrieved. Applications must release returned pointer(s) when they are no longer needed, or else there will be a memory leak.

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
