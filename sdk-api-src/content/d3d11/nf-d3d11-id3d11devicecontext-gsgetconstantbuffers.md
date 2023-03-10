---
UID: NF:d3d11.ID3D11DeviceContext.GSGetConstantBuffers
title: ID3D11DeviceContext::GSGetConstantBuffers (d3d11.h)
description: Get the constant buffers used by the geometry shader pipeline stage. (ID3D11DeviceContext.GSGetConstantBuffers)
helpviewer_keywords: ["90cf0266-e4b2-8106-f337-5c65752dd7d8","GSGetConstantBuffers","GSGetConstantBuffers method [Direct3D 11]","GSGetConstantBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GSGetConstantBuffers method","ID3D11DeviceContext.GSGetConstantBuffers","ID3D11DeviceContext::GSGetConstantBuffers","d3d11/ID3D11DeviceContext::GSGetConstantBuffers","direct3d11.id3d11devicecontext_gsgetconstantbuffers"]
old-location: direct3d11\id3d11devicecontext_gsgetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 1a28c673-1e37-4801-bb9c-ba0cf28335d1
ms.date: 12/05/2018
ms.keywords: 90cf0266-e4b2-8106-f337-5c65752dd7d8, GSGetConstantBuffers, GSGetConstantBuffers method [Direct3D 11], GSGetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSGetConstantBuffers method, ID3D11DeviceContext.GSGetConstantBuffers, ID3D11DeviceContext::GSGetConstantBuffers, d3d11/ID3D11DeviceContext::GSGetConstantBuffers, direct3d11.id3d11devicecontext_gsgetconstantbuffers
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
 - ID3D11DeviceContext::GSGetConstantBuffers
 - d3d11/ID3D11DeviceContext::GSGetConstantBuffers
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
 - ID3D11DeviceContext.GSGetConstantBuffers
---

# ID3D11DeviceContext::GSGetConstantBuffers


## -description

Get the constant buffers used by the geometry shader pipeline stage.

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
