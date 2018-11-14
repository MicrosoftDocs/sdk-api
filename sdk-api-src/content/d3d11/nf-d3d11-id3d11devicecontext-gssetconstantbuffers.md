---
UID: NF:d3d11.ID3D11DeviceContext.GSSetConstantBuffers
title: ID3D11DeviceContext::GSSetConstantBuffers
author: windows-sdk-content
description: Sets the constant buffers used by the geometry shader pipeline stage.
old-location: direct3d11\id3d11devicecontext_gssetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 2af7ab0c-4a21-474c-9a17-ed90f89285fd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GSSetConstantBuffers, GSSetConstantBuffers method [Direct3D 11], GSSetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSSetConstantBuffers method, ID3D11DeviceContext.GSSetConstantBuffers, ID3D11DeviceContext::GSSetConstantBuffers, ad892eb6-e3c1-f7c2-8552-c1feae8690bc, d3d11/ID3D11DeviceContext::GSSetConstantBuffers, direct3d11.id3d11devicecontext_gssetconstantbuffers
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
 - ID3D11DeviceContext.GSSetConstantBuffers
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
- ID3D11DeviceContext.GSSetConstantBuffers
: 
---

# ID3D11DeviceContext::GSSetConstantBuffers


## -description


Sets the constant buffers used by the geometry shader pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into the device's zero-based array to begin setting constant buffers to (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - 1).


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of buffers to set (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - <i>StartSlot</i>).


### -param ppConstantBuffers [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>*</b>

Array of constant buffers (see <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>) being given to the device.


## -returns



This method does not return a value.




## -remarks



The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

You can't use the <a href="https://msdn.microsoft.com/en-us/library/Ff476591(v=VS.85).aspx">ID3D11ShaderReflectionConstantBuffer</a> interface to get information about what is currently bound to the pipeline in the device context. But you can use <b>ID3D11ShaderReflectionConstantBuffer</b> to get information from a compiled shader. For example, you can use <b>ID3D11ShaderReflectionConstantBuffer</b> and <a href="https://msdn.microsoft.com/en-us/library/Ff476607(v=VS.85).aspx">ID3D11ShaderReflectionVariable</a> to determine the slot in which a geometry shader expects a constant buffer. You can then pass this slot number to <b>GSSetConstantBuffers</b> to set the constant buffer. You can call the <a href="https://msdn.microsoft.com/en-us/library/Ff728670(v=VS.85).aspx">D3D11Reflect</a> function to retrieve the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Ff476590(v=VS.85).aspx">ID3D11ShaderReflection</a> interface and then call <a href="https://msdn.microsoft.com/en-us/library/Ff476613(v=VS.85).aspx">ID3D11ShaderReflection::GetConstantBufferByName</a> to get a pointer to <b>ID3D11ShaderReflectionConstantBuffer</b>.

The Direct3D 11.1 runtime, which is available starting with Windows 8, can bind a larger number of <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a> resources to the shader than the maximum constant buffer size that is supported by shaders (4096 constants – 4*32-bit components each).  When you bind such a large buffer, the shader can access only the first 4096 4*32-bit component constants in the buffer, as if 4096 constants is the full size of the buffer.  

If the application wants the shader to access other parts of the buffer, it must call the <a href="https://msdn.microsoft.com/en-us/library/Hh404638(v=VS.85).aspx">GSSetConstantBuffers1</a> method instead. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

