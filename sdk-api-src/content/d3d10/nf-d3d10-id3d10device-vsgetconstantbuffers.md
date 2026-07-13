---
UID: NF:d3d10.ID3D10Device.VSGetConstantBuffers
title: ID3D10Device::VSGetConstantBuffers (d3d10.h)
description: Get the constant buffers used by the vertex shader pipeline stage. (ID3D10Device.VSGetConstantBuffers)
helpviewer_keywords: ["2359bc62-0205-acb7-f462-1ceafd1f8b80","ID3D10Device interface [Direct3D 10]","VSGetConstantBuffers method","ID3D10Device.VSGetConstantBuffers","ID3D10Device::VSGetConstantBuffers","VSGetConstantBuffers","VSGetConstantBuffers method [Direct3D 10]","VSGetConstantBuffers method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::VSGetConstantBuffers","direct3d10.id3d10device_vsgetconstantbuffers"]
old-location: direct3d10\id3d10device_vsgetconstantbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vsgetconstantbuffers.htm
ms.date: 12/05/2018
ms.keywords: 2359bc62-0205-acb7-f462-1ceafd1f8b80, ID3D10Device interface [Direct3D 10],VSGetConstantBuffers method, ID3D10Device.VSGetConstantBuffers, ID3D10Device::VSGetConstantBuffers, VSGetConstantBuffers, VSGetConstantBuffers method [Direct3D 10], VSGetConstantBuffers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSGetConstantBuffers, direct3d10.id3d10device_vsgetconstantbuffers
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
 - ID3D10Device::VSGetConstantBuffers
 - d3d10/ID3D10Device::VSGetConstantBuffers
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
 - ID3D10Device.VSGetConstantBuffers
---

# ID3D10Device::VSGetConstantBuffers


## -description

Get the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="/previous-versions/bb205146(v=vs.85)">vertex shader</a> pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from.

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to retrieve.

### -param ppConstantBuffers [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>) to be returned by the method.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
