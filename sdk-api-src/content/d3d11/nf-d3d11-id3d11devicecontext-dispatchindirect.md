---
UID: NF:d3d11.ID3D11DeviceContext.DispatchIndirect
title: ID3D11DeviceContext::DispatchIndirect (d3d11.h)
description: Execute a command list over one or more thread groups.
helpviewer_keywords: ["4aaa5960-b4f6-bccf-2256-435d0fef6be6","DispatchIndirect","DispatchIndirect method [Direct3D 11]","DispatchIndirect method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DispatchIndirect method","ID3D11DeviceContext.DispatchIndirect","ID3D11DeviceContext::DispatchIndirect","d3d11/ID3D11DeviceContext::DispatchIndirect","direct3d11.id3d11devicecontext_dispatchindirect"]
old-location: direct3d11\id3d11devicecontext_dispatchindirect.htm
tech.root: direct3d11
ms.assetid: bb8840f5-ae4b-42d6-b51d-6844d0b18074
ms.date: 12/05/2018
ms.keywords: 4aaa5960-b4f6-bccf-2256-435d0fef6be6, DispatchIndirect, DispatchIndirect method [Direct3D 11], DispatchIndirect method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DispatchIndirect method, ID3D11DeviceContext.DispatchIndirect, ID3D11DeviceContext::DispatchIndirect, d3d11/ID3D11DeviceContext::DispatchIndirect, direct3d11.id3d11devicecontext_dispatchindirect
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
 - ID3D11DeviceContext::DispatchIndirect
 - d3d11/ID3D11DeviceContext::DispatchIndirect
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
 - ID3D11DeviceContext.DispatchIndirect
---

# ID3D11DeviceContext::DispatchIndirect


## -description

Execute a command list over one or more thread groups.

## -parameters

### -param pBufferForArgs [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>, which must be loaded with data that matches the argument list for <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">ID3D11DeviceContext::Dispatch</a>.

### -param AlignedByteOffsetForArgs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A byte-aligned offset between the start of the buffer and the arguments.

## -remarks

You call the <b>DispatchIndirect</b> method to execute commands in a <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader">compute shader</a>.

When an application creates a buffer that is associated with the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> interface that  <i>pBufferForArgs</i> points to, the application must set the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS</a> flag in the <b>MiscFlags</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a> structure that describes the buffer. To create the buffer, the application calls the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createbuffer">ID3D11Device::CreateBuffer</a> method and in this call passes a pointer to <b>D3D11_BUFFER_DESC</b> in the <i>pDesc</i> parameter.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>