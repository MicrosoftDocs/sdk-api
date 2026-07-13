---
UID: NF:d3d11.ID3D11DeviceContext.PSGetSamplers
title: ID3D11DeviceContext::PSGetSamplers (d3d11.h)
description: Get an array of sampler states from the pixel shader pipeline stage. (ID3D11DeviceContext.PSGetSamplers)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","PSGetSamplers method","ID3D11DeviceContext.PSGetSamplers","ID3D11DeviceContext::PSGetSamplers","PSGetSamplers","PSGetSamplers method [Direct3D 11]","PSGetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::PSGetSamplers","direct3d11.id3d11devicecontext_psgetsamplers","ffce57e5-f18e-d0e2-8fb6-4ee3acfcbb90"]
old-location: direct3d11\id3d11devicecontext_psgetsamplers.htm
tech.root: direct3d11
ms.assetid: 8a86f6c8-4095-48d5-a3aa-a3eef9f4b3e8
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],PSGetSamplers method, ID3D11DeviceContext.PSGetSamplers, ID3D11DeviceContext::PSGetSamplers, PSGetSamplers, PSGetSamplers method [Direct3D 11], PSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSGetSamplers, direct3d11.id3d11devicecontext_psgetsamplers, ffce57e5-f18e-d0e2-8fb6-4ee3acfcbb90
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
 - ID3D11DeviceContext::PSGetSamplers
 - d3d11/ID3D11DeviceContext::PSGetSamplers
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
 - ID3D11DeviceContext.PSGetSamplers
---

# ID3D11DeviceContext::PSGetSamplers


## -description

Get an array of sampler states from the pixel shader pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into a zero-based array to begin getting samplers from (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).

### -param NumSamplers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers to get from a device context. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).

### -param ppSamplers [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>**</b>

Array of sampler-state interface pointers (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>) to be returned by the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
