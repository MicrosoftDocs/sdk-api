---
UID: NF:d3d11.ID3D11DeviceContext.DSGetSamplers
title: ID3D11DeviceContext::DSGetSamplers (d3d11.h)
description: Get an array of sampler state interfaces from the domain-shader stage.
helpviewer_keywords: ["070d6004-b3cb-bc84-b78f-d7f9851d5fbf","DSGetSamplers","DSGetSamplers method [Direct3D 11]","DSGetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DSGetSamplers method","ID3D11DeviceContext.DSGetSamplers","ID3D11DeviceContext::DSGetSamplers","d3d11/ID3D11DeviceContext::DSGetSamplers","direct3d11.id3d11devicecontext_dsgetsamplers"]
old-location: direct3d11\id3d11devicecontext_dsgetsamplers.htm
tech.root: direct3d11
ms.assetid: 9cb6fee7-0dda-472c-b2e0-36d52e7f12b7
ms.date: 12/05/2018
ms.keywords: 070d6004-b3cb-bc84-b78f-d7f9851d5fbf, DSGetSamplers, DSGetSamplers method [Direct3D 11], DSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSGetSamplers method, ID3D11DeviceContext.DSGetSamplers, ID3D11DeviceContext::DSGetSamplers, d3d11/ID3D11DeviceContext::DSGetSamplers, direct3d11.id3d11devicecontext_dsgetsamplers
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
 - ID3D11DeviceContext::DSGetSamplers
 - d3d11/ID3D11DeviceContext::DSGetSamplers
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
 - ID3D11DeviceContext.DSGetSamplers
---

# ID3D11DeviceContext::DSGetSamplers


## -description

Get an array of sampler state interfaces from the domain-shader stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into a zero-based array to begin getting samplers from (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).

### -param NumSamplers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers to get from a device context. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).

### -param ppSamplers [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>**</b>

Pointer to an array of sampler-state interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>).

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>