---
UID: NF:d3d11.ID3D11DeviceContext.CSGetSamplers
title: ID3D11DeviceContext::CSGetSamplers (d3d11.h)
description: Get an array of sampler state interfaces from the compute-shader stage.
helpviewer_keywords: ["727801db-5fe0-a11b-bb2e-70ee26a54119","CSGetSamplers","CSGetSamplers method [Direct3D 11]","CSGetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSGetSamplers method","ID3D11DeviceContext.CSGetSamplers","ID3D11DeviceContext::CSGetSamplers","d3d11/ID3D11DeviceContext::CSGetSamplers","direct3d11.id3d11devicecontext_csgetsamplers"]
old-location: direct3d11\id3d11devicecontext_csgetsamplers.htm
tech.root: direct3d11
ms.assetid: 97f5be84-3562-4b5a-9c7a-2ac3f18a184b
ms.date: 12/05/2018
ms.keywords: 727801db-5fe0-a11b-bb2e-70ee26a54119, CSGetSamplers, CSGetSamplers method [Direct3D 11], CSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSGetSamplers method, ID3D11DeviceContext.CSGetSamplers, ID3D11DeviceContext::CSGetSamplers, d3d11/ID3D11DeviceContext::CSGetSamplers, direct3d11.id3d11devicecontext_csgetsamplers
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
 - ID3D11DeviceContext::CSGetSamplers
 - d3d11/ID3D11DeviceContext::CSGetSamplers
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
 - ID3D11DeviceContext.CSGetSamplers
---

# ID3D11DeviceContext::CSGetSamplers


## -description

Get an array of sampler state interfaces from the compute-shader stage.

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