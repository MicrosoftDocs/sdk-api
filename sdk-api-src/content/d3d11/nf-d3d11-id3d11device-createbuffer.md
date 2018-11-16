---
UID: NF:d3d11.ID3D11Device.CreateBuffer
title: ID3D11Device::CreateBuffer
author: windows-sdk-content
description: Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).
old-location: direct3d11\id3d11device_createbuffer.htm
tech.root: direct3d11
ms.assetid: 5aec93c5-12a1-4b4e-813e-ee1e85adbf14
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateBuffer, CreateBuffer method [Direct3D 11], CreateBuffer method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateBuffer method, ID3D11Device.CreateBuffer, ID3D11Device::CreateBuffer, d3d11/ID3D11Device::CreateBuffer, direct3d11.id3d11device_createbuffer, e4ddf93d-90c3-2369-284d-e5d67efaf51e
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11Device.CreateBuffer
: 
---

# ID3D11Device::CreateBuffer


## -description


Creates a buffer (vertex buffer, index buffer, or shader-constant buffer).


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a> structure that describes the buffer.
          


### -param pInitialData [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/0ae10f12-4ef7-4dab-a7d7-fb4f2fd72a73">D3D11_SUBRESOURCE_DATA</a> structure that describes  the initialization data;
            use <b>NULL</b> to allocate space only (with the exception that it cannot be <b>NULL</b> if the usage flag is <b>D3D11_USAGE_IMMUTABLE</b>).
            

If you don't pass anything to <i>pInitialData</i>, the initial content of the memory for the buffer is undefined.
              In this case, you need to write the buffer content some other way before the resource is read.
            


### -param ppBuffer [out, optional]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>**</b>

Address of a pointer to the <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a> interface for the buffer object created.
            Set this parameter to <b>NULL</b> to validate the other input parameters (<b>S_FALSE</b> indicates a pass).
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the buffer.
              See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.
            




## -remarks



For example code, see <a href="https://msdn.microsoft.com/584a39d1-7629-429a-b451-64b1432cb48f">How to: Create a Vertex Buffer</a>,
          <a href="https://msdn.microsoft.com/4b33d32a-27fd-4652-87ac-3b7268881f89">How to: Create an Index Buffer</a> or 
          <a href="https://msdn.microsoft.com/78694ac2-e850-402d-8c99-6afb0bd5d660">How to: Create a Constant Buffer</a>.
        

For a constant buffer (<b>BindFlags</b> of  <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a> set to <a href="d3d11_bind_flag.htm">D3D11_BIND_CONSTANT_BUFFER</a>), 
          you must set the <b>ByteWidth</b> value of  <b>D3D11_BUFFER_DESC</b> in multiples of 16, and less than or equal to <b>D3D11_REQ_CONSTANT_BUFFER_ELEMENT_COUNT</b>.
        

The Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems, provides the following new functionality for <b>CreateBuffer</b>:
        

You can create a constant buffer that is larger than the maximum constant buffer size that a shader can access (4096 32-bit*4-component constants – 64KB).
          When you bind the constant buffer to the pipeline (for example, via <a href="https://msdn.microsoft.com/03e5f255-3a5d-4c77-ad3b-5a188c9eb35b">PSSetConstantBuffers</a> or <a href="https://msdn.microsoft.com/4B05144B-7766-4AE6-9B9F-C439B4BF0220">PSSetConstantBuffers1</a>), 
          you can define a range of the buffer that the shader can access that fits within the 4096 constant limit.
        

The runtime will emulate this feature for <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 9.1, 9.2, and 9.3; therefore, this feature is supported for feature level 9.1, 9.2, and 9.3.
          This feature is always available on new drivers for feature level 10 and higher.
          On existing drivers that are implemented to feature level 10 and higher, a call to <b>CreateBuffer</b> to request a constant buffer that is larger than 4096 fails.
        




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

