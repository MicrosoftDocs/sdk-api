---
UID: NF:d3d10.ID3D10Device.CreateBuffer
title: ID3D10Device::CreateBuffer (d3d10.h)
description: Create a buffer (vertex buffer, index buffer, or shader-constant buffer).
helpviewer_keywords: ["CreateBuffer","CreateBuffer method [Direct3D 10]","CreateBuffer method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateBuffer method","ID3D10Device.CreateBuffer","ID3D10Device::CreateBuffer","d3d10/ID3D10Device::CreateBuffer","direct3d10.id3d10device_createbuffer","f67833a5-95f8-0430-5015-e074533c6dd1"]
old-location: direct3d10\id3d10device_createbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createbuffer.htm
ms.date: 12/05/2018
ms.keywords: CreateBuffer, CreateBuffer method [Direct3D 10], CreateBuffer method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateBuffer method, ID3D10Device.CreateBuffer, ID3D10Device::CreateBuffer, d3d10/ID3D10Device::CreateBuffer, direct3d10.id3d10device_createbuffer, f67833a5-95f8-0430-5015-e074533c6dd1
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
 - ID3D10Device::CreateBuffer
 - d3d10/ID3D10Device::CreateBuffer
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
 - ID3D10Device.CreateBuffer
---

# ID3D10Device::CreateBuffer


## -description

Create a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a> (vertex buffer, index buffer, or shader-constant buffer).

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">D3D10_BUFFER_DESC</a>*</b>

Pointer to a buffer description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">D3D10_BUFFER_DESC</a>).

### -param pInitialData [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_subresource_data">D3D10_SUBRESOURCE_DATA</a>*</b>

Pointer to the initialization data (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_subresource_data">D3D10_SUBRESOURCE_DATA</a>); use <b>NULL</b> to allocate space only.

### -param ppBuffer [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>**</b>

Address of a pointer to the buffer created (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer Interface</a>). Set this parameter to <b>NULL</b> to validate the other input parameters (S_FALSE indicates a pass).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

For example code, see:

<ul>
<li>
<a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Create a Vertex Buffer</a>
</li>
<li>
<a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating">Create an Index Buffer</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>