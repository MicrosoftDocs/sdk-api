---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexedInstancedIndirect
title: ID3D11DeviceContext::DrawIndexedInstancedIndirect (d3d11.h)
description: Draw indexed, instanced, GPU-generated primitives.
helpviewer_keywords: ["490eea55-c4b9-bcfb-1fd8-021b92e7979d","DrawIndexedInstancedIndirect","DrawIndexedInstancedIndirect method [Direct3D 11]","DrawIndexedInstancedIndirect method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DrawIndexedInstancedIndirect method","ID3D11DeviceContext.DrawIndexedInstancedIndirect","ID3D11DeviceContext::DrawIndexedInstancedIndirect","d3d11/ID3D11DeviceContext::DrawIndexedInstancedIndirect","direct3d11.id3d11devicecontext_drawindexedinstancedindirect"]
old-location: direct3d11\id3d11devicecontext_drawindexedinstancedindirect.htm
tech.root: direct3d11
ms.assetid: c6969210-b452-4a49-a3d7-d849b1d2ebb5
ms.date: 02/02/2022
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
 - ID3D11DeviceContext::DrawIndexedInstancedIndirect
 - d3d11/ID3D11DeviceContext::DrawIndexedInstancedIndirect
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
 - ID3D11DeviceContext.DrawIndexedInstancedIndirect
---

## -description

Draw indexed, instanced, GPU-generated primitives.

## -parameters

### -param pBufferForArgs [in]

Type: **[ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer)\***

A pointer to an [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer), which is a buffer containing the GPU-generated primitives.

### -param AlignedByteOffsetForArgs [in]

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

A DWORD-aligned byte offset in <i>pBufferForArgs</i> to the start of the GPU generated primitives.

## -remarks

When an application creates a buffer that is associated with the [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interface that *pBufferForArgs* points to, your application must set the [D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag in the *MiscFlags* member of the [D3D11_BUFFER_DESC](/windows/win32/api/d3d11/ns-d3d11-d3d11_buffer_desc) structure that describes the buffer. To create the buffer, your application should call the [ID3D11Device::CreateBuffer](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer) method, and pass a pointer to a **D3D11_BUFFER_DESC** in the *pDesc* parameter.

**Windows Phone 8:** This API is supported.

## -see-also

[ID3D11DeviceContext](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext)
