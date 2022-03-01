---
UID: NF:d3d11.ID3D11DeviceContext.CSSetConstantBuffers
title: ID3D11DeviceContext::CSSetConstantBuffers (d3d11.h)
description: Sets the constant buffers used by the compute-shader stage.
helpviewer_keywords: ["75636b6c-7b80-b606-530c-50b7b27df917","CSSetConstantBuffers","CSSetConstantBuffers method [Direct3D 11]","CSSetConstantBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSSetConstantBuffers method","ID3D11DeviceContext.CSSetConstantBuffers","ID3D11DeviceContext::CSSetConstantBuffers","d3d11/ID3D11DeviceContext::CSSetConstantBuffers","direct3d11.id3d11devicecontext_cssetconstantbuffers"]
old-location: direct3d11\id3d11devicecontext_cssetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 40970d1d-bad3-48e0-8f0e-6d45fe602594
ms.date: 12/05/2018
ms.keywords: 75636b6c-7b80-b606-530c-50b7b27df917, CSSetConstantBuffers, CSSetConstantBuffers method [Direct3D 11], CSSetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSSetConstantBuffers method, ID3D11DeviceContext.CSSetConstantBuffers, ID3D11DeviceContext::CSSetConstantBuffers, d3d11/ID3D11DeviceContext::CSSetConstantBuffers, direct3d11.id3d11devicecontext_cssetconstantbuffers
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
 - ID3D11DeviceContext::CSSetConstantBuffers
 - d3d11/ID3D11DeviceContext::CSSetConstantBuffers
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
 - ID3D11DeviceContext.CSSetConstantBuffers
---

# ID3D11DeviceContext::CSSetConstantBuffers


## -description

Sets the constant buffers used by the compute-shader stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the zero-based array to begin setting constant buffers to (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - 1).

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to set (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - <i>StartSlot</i>).

### -param ppConstantBuffers [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

Array of constant buffers (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>) being given to the device.

## -remarks

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

The Direct3D 11.1 runtime, which is available starting with Windows 8, can bind a larger number of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> resources to the shader than the maximum constant buffer size that is supported by shaders (4096 constants – 4\*32-bit components each).  When you bind such a large buffer, the shader can access only the first 4096 4\*32-bit component constants in the buffer, as if 4096 constants is the full size of the buffer.  

If the application wants the shader to access other parts of the buffer, it must call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1">CSSetConstantBuffers1</a> method instead.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
