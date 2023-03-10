---
UID: NF:d3d11.ID3D11DeviceContext.VSGetSamplers
title: ID3D11DeviceContext::VSGetSamplers (d3d11.h)
description: Get an array of sampler states from the vertex shader pipeline stage. (ID3D11DeviceContext.VSGetSamplers)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","VSGetSamplers method","ID3D11DeviceContext.VSGetSamplers","ID3D11DeviceContext::VSGetSamplers","VSGetSamplers","VSGetSamplers method [Direct3D 11]","VSGetSamplers method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::VSGetSamplers","da7916b1-64dc-68da-7790-065a4977bd36","direct3d11.id3d11devicecontext_vsgetsamplers"]
old-location: direct3d11\id3d11devicecontext_vsgetsamplers.htm
tech.root: direct3d11
ms.assetid: 0b8cbdfe-58e1-46f0-86c1-22da8178d296
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],VSGetSamplers method, ID3D11DeviceContext.VSGetSamplers, ID3D11DeviceContext::VSGetSamplers, VSGetSamplers, VSGetSamplers method [Direct3D 11], VSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::VSGetSamplers, da7916b1-64dc-68da-7790-065a4977bd36, direct3d11.id3d11devicecontext_vsgetsamplers
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
 - ID3D11DeviceContext::VSGetSamplers
 - d3d11/ID3D11DeviceContext::VSGetSamplers
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
 - ID3D11DeviceContext.VSGetSamplers
---

# ID3D11DeviceContext::VSGetSamplers


## -description

Get an array of sampler states from the vertex shader pipeline stage.

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
