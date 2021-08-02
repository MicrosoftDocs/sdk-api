---
UID: NF:d3d10.ID3D10Device.GSGetSamplers
title: ID3D10Device::GSGetSamplers (d3d10.h)
description: Get an array of sampler states from the geometry shader pipeline stage.
helpviewer_keywords: ["GSGetSamplers","GSGetSamplers method [Direct3D 10]","GSGetSamplers method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GSGetSamplers method","ID3D10Device.GSGetSamplers","ID3D10Device::GSGetSamplers","d3d10/ID3D10Device::GSGetSamplers","d4899d8d-c796-58f0-bf8b-42bb650492dc","direct3d10.id3d10device_gsgetsamplers"]
old-location: direct3d10\id3d10device_gsgetsamplers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gsgetsamplers.htm
ms.date: 12/05/2018
ms.keywords: GSGetSamplers, GSGetSamplers method [Direct3D 10], GSGetSamplers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSGetSamplers method, ID3D10Device.GSGetSamplers, ID3D10Device::GSGetSamplers, d3d10/ID3D10Device::GSGetSamplers, d4899d8d-c796-58f0-bf8b-42bb650492dc, direct3d10.id3d10device_gsgetsamplers
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
 - ID3D10Device::GSGetSamplers
 - d3d10/ID3D10Device::GSGetSamplers
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
 - ID3D10Device.GSGetSamplers
---

# ID3D10Device::GSGetSamplers


## -description

Get an array of sampler states from the <a href="/previous-versions/bb205146(v=vs.85)">geometry shader</a> pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin getting samplers from.

### -param NumSamplers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of samplers to get from the device. Each pipeline stage has a total of 16 sampler slots available.

### -param ppSamplers [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>**</b>

Array of sampler-state pointers (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10samplerstate">ID3D10SamplerState</a>) to be returned by the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>