---
UID: NF:d3d11.ID3D11DeviceContext.VSGetConstantBuffers
title: ID3D11DeviceContext::VSGetConstantBuffers (d3d11.h)
description: Get the constant buffers used by the vertex shader pipeline stage. (ID3D11DeviceContext.VSGetConstantBuffers)
helpviewer_keywords: ["195aec78-0809-915e-4807-c20139d72b2b","ID3D11DeviceContext interface [Direct3D 11]","VSGetConstantBuffers method","ID3D11DeviceContext.VSGetConstantBuffers","ID3D11DeviceContext::VSGetConstantBuffers","VSGetConstantBuffers","VSGetConstantBuffers method [Direct3D 11]","VSGetConstantBuffers method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::VSGetConstantBuffers","direct3d11.id3d11devicecontext_vsgetconstantbuffers"]
old-location: direct3d11\id3d11devicecontext_vsgetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: d31bff37-4109-40af-bc75-7e73582d6fa1
ms.date: 12/05/2018
ms.keywords: 195aec78-0809-915e-4807-c20139d72b2b, ID3D11DeviceContext interface [Direct3D 11],VSGetConstantBuffers method, ID3D11DeviceContext.VSGetConstantBuffers, ID3D11DeviceContext::VSGetConstantBuffers, VSGetConstantBuffers, VSGetConstantBuffers method [Direct3D 11], VSGetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::VSGetConstantBuffers, direct3d11.id3d11devicecontext_vsgetconstantbuffers
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
 - ID3D11DeviceContext::VSGetConstantBuffers
 - d3d11/ID3D11DeviceContext::VSGetConstantBuffers
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
 - ID3D11DeviceContext.VSGetConstantBuffers
---

# ID3D11DeviceContext::VSGetConstantBuffers


## -description

Get the constant buffers used by the vertex shader pipeline stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - 1).

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to retrieve (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - StartSlot).

### -param ppConstantBuffers [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>) to be returned by the method.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
