---
UID: NF:d3d11.ID3D11DeviceContext.HSGetConstantBuffers
title: ID3D11DeviceContext::HSGetConstantBuffers (d3d11.h)
description: Get the constant buffers used by the hull-shader stage.
helpviewer_keywords: ["46eee6d7-9ce0-ef7b-68bd-2f0c8f0b3136","HSGetConstantBuffers","HSGetConstantBuffers method [Direct3D 11]","HSGetConstantBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","HSGetConstantBuffers method","ID3D11DeviceContext.HSGetConstantBuffers","ID3D11DeviceContext::HSGetConstantBuffers","d3d11/ID3D11DeviceContext::HSGetConstantBuffers","direct3d11.id3d11devicecontext_hsgetconstantbuffers"]
old-location: direct3d11\id3d11devicecontext_hsgetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 82987afa-fcb4-4d87-ab53-916a9dac3609
ms.date: 12/05/2018
ms.keywords: 46eee6d7-9ce0-ef7b-68bd-2f0c8f0b3136, HSGetConstantBuffers, HSGetConstantBuffers method [Direct3D 11], HSGetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSGetConstantBuffers method, ID3D11DeviceContext.HSGetConstantBuffers, ID3D11DeviceContext::HSGetConstantBuffers, d3d11/ID3D11DeviceContext::HSGetConstantBuffers, direct3d11.id3d11devicecontext_hsgetconstantbuffers
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
 - ID3D11DeviceContext::HSGetConstantBuffers
 - d3d11/ID3D11DeviceContext::HSGetConstantBuffers
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
 - ID3D11DeviceContext.HSGetConstantBuffers
---

# ID3D11DeviceContext::HSGetConstantBuffers


## -description

Get the constant buffers used by the <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation">hull-shader stage</a>.

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