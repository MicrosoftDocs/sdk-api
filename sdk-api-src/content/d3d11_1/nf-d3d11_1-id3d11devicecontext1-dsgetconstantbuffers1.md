---
UID: NF:d3d11_1.ID3D11DeviceContext1.DSGetConstantBuffers1
title: ID3D11DeviceContext1::DSGetConstantBuffers1 (d3d11_1.h)
description: Gets the constant buffers that the domain-shader stage uses.
helpviewer_keywords: ["DSGetConstantBuffers1","DSGetConstantBuffers1 method [Direct3D 11]","DSGetConstantBuffers1 method [Direct3D 11]","ID3D11DeviceContext1 interface","ID3D11DeviceContext1 interface [Direct3D 11]","DSGetConstantBuffers1 method","ID3D11DeviceContext1.DSGetConstantBuffers1","ID3D11DeviceContext1::DSGetConstantBuffers1","d3d11_1/ID3D11DeviceContext1::DSGetConstantBuffers1","direct3d11.id3d11devicecontext1_dsgetconstantbuffers1"]
old-location: direct3d11\id3d11devicecontext1_dsgetconstantbuffers1.htm
tech.root: direct3d11
ms.assetid: 7C6E2BFF-E351-417C-B351-F9B8EDB95F57
ms.date: 12/05/2018
ms.keywords: DSGetConstantBuffers1, DSGetConstantBuffers1 method [Direct3D 11], DSGetConstantBuffers1 method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DSGetConstantBuffers1 method, ID3D11DeviceContext1.DSGetConstantBuffers1, ID3D11DeviceContext1::DSGetConstantBuffers1, d3d11_1/ID3D11DeviceContext1::DSGetConstantBuffers1, direct3d11.id3d11devicecontext1_dsgetconstantbuffers1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11DeviceContext1::DSGetConstantBuffers1
 - d3d11_1/ID3D11DeviceContext1::DSGetConstantBuffers1
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
 - ID3D11DeviceContext1.DSGetConstantBuffers1
---

# ID3D11DeviceContext1::DSGetConstantBuffers1


## -description

Gets the constant buffers that the domain-shader stage uses.

## -parameters

### -param StartSlot [in]

Index into the device's zero-based array to begin retrieving constant buffers from (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - 1).

### -param NumBuffers [in]

Number of buffers to retrieve (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - <i>StartSlot</i>).

### -param ppConstantBuffers [out, optional]

Array of constant buffer interface pointers to be returned by the method.

### -param pFirstConstant [out, optional]

A pointer to an array that receives the offsets into the buffers that  <i>ppConstantBuffers</i> specifies. Each offset specifies where, from the shader's point of view, each constant buffer starts.  Each offset is measured in shader constants, which are 16 bytes (4*32-bit components).  Therefore, an offset of 2 indicates that the start of the associated constant buffer is 32 bytes into the constant buffer. The runtime sets <i>pFirstConstant</i> to <b>NULL</b> if the buffers do not have offsets.

### -param pNumConstants [out, optional]

A pointer to an array that receives the numbers of constants in the buffers that  <i>ppConstantBuffers</i> specifies. Each number specifies the number of constants that are contained in the constant buffer that the shader uses. Each number of constants starts from its respective offset that is specified in the <i>pFirstConstant</i> array. The runtime sets <i>pNumConstants</i> to <b>NULL</b> if it doesn't specify the numbers of constants in each buffer.

## -remarks

If no buffer is bound at a slot, <i>pFirstConstant</i> and <i>pNumConstants</i> are <b>NULL</b> for that slot.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>