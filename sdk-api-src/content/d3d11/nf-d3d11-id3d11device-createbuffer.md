---
UID: NF:d3d11.ID3D11Device.CreateBuffer
title: ID3D11Device::CreateBuffer (d3d11.h)
description: Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).
helpviewer_keywords: ["CreateBuffer","CreateBuffer method [Direct3D 11]","CreateBuffer method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateBuffer method","ID3D11Device.CreateBuffer","ID3D11Device::CreateBuffer","d3d11/ID3D11Device::CreateBuffer","direct3d11.id3d11device_createbuffer","e4ddf93d-90c3-2369-284d-e5d67efaf51e"]
old-location: direct3d11\id3d11device_createbuffer.htm
tech.root: direct3d11
ms.assetid: 5aec93c5-12a1-4b4e-813e-ee1e85adbf14
ms.date: 12/05/2018
ms.keywords: CreateBuffer, CreateBuffer method [Direct3D 11], CreateBuffer method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateBuffer method, ID3D11Device.CreateBuffer, ID3D11Device::CreateBuffer, d3d11/ID3D11Device::CreateBuffer, direct3d11.id3d11device_createbuffer, e4ddf93d-90c3-2369-284d-e5d67efaf51e
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
 - ID3D11Device::CreateBuffer
 - d3d11/ID3D11Device::CreateBuffer
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
 - ID3D11Device.CreateBuffer
---

# ID3D11Device::CreateBuffer


## -description

Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a> structure that describes the buffer.

### -param pInitialData [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_subresource_data">D3D11_SUBRESOURCE_DATA</a> structure that describes  the initialization data;
            use <b>NULL</b> to allocate space only (with the exception that it cannot be <b>NULL</b> if the usage flag is <b>D3D11_USAGE_IMMUTABLE</b>).
            

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the buffer is undefined.
              In this case, you need to write the buffer content some other way before the resource is read.

### -param ppBuffer [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>**</b>

Address of a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> interface for the buffer object created.
            Set this parameter to <b>NULL</b> to validate the other input parameters (<b>S_FALSE</b> indicates a pass).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the buffer.
              See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a> for other possible return values.

## -remarks

For example code, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to">How to: Create a Vertex Buffer</a>,
          <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to">How to: Create an Index Buffer</a> or 
          <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to">How to: Create a Constant Buffer</a>.
        

For a constant buffer (<b>BindFlags</b> of  <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a> set to <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_CONSTANT_BUFFER</a>), 
          you must set the <b>ByteWidth</b> value of  <b>D3D11_BUFFER_DESC</b> in multiples of 16, and less than or equal to <b>D3D11_REQ_CONSTANT_BUFFER_ELEMENT_COUNT</b>.
        

The Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems, provides the following new functionality for <b>CreateBuffer</b>:
        

You can create a constant buffer that is larger than the maximum constant buffer size that a shader can access (4096 32-bit*4-component constants – 64KB).
          When you bind the constant buffer to the pipeline (for example, via <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers">PSSetConstantBuffers</a> or <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1">PSSetConstantBuffers1</a>), 
          you can define a range of the buffer that the shader can access that fits within the 4096 constant limit.
        
The Direct3D 11.1 runtime (available in Windows 8 and later operating systems) emulates this feature for [feature level](/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.1, 9.2, and 9.3; therefore, this feature is supported for feature level 9.1, 9.2, and 9.3.

This feature is always available on new drivers for feature level 10 and higher.

On runtimes older than Direct3D 11.1, a call to **CreateBuffer** to request a constant buffer that is larger than 4096 fails.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>