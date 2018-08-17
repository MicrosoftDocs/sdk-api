---
UID: NF:d3d10.ID3D10Device.CreateInputLayout
title: ID3D10Device::CreateInputLayout
author: windows-sdk-content
description: Create an input-layout object to describe the input-buffer data for the input-assembler stage.
old-location: direct3d10\id3d10device_createinputlayout.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createinputlayout.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 1535092d-4b37-123e-52db-51ce771e66b9, CreateInputLayout, CreateInputLayout method [Direct3D 10], CreateInputLayout method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateInputLayout method, ID3D10Device.CreateInputLayout, ID3D10Device::CreateInputLayout, d3d10/ID3D10Device::CreateInputLayout, direct3d10.id3d10device_createinputlayout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateInputLayout
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateInputLayout


## -description


Create an input-layout object to describe the input-buffer data for the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


## -parameters




### -param pInputElementDescs [in]

Type: <b>const <a href="https://msdn.microsoft.com/b1d65bf3-5a94-4831-854b-dd124b663975">D3D10_INPUT_ELEMENT_DESC</a>*</b>

An array of the input-assembler stage input data types; each type is described by an element description (see <a href="https://msdn.microsoft.com/b1d65bf3-5a94-4831-854b-dd124b663975">D3D10_INPUT_ELEMENT_DESC</a>).


### -param NumElements [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of input-data types in the array of input-elements.


### -param pShaderBytecodeWithInputSignature [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://msdn.microsoft.com/cff6f901-cb9b-44d5-a75b-9a4029a37215">Getting a Pointer to a Compiled Shader</a>. The compiled shader code contains a <a href="https://msdn.microsoft.com/c73a4f3e-e6fa-4e49-9ee8-4e200269dba7">input signature</a> which is validated against the array of elements. See remarks.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled shader.


### -param ppInputLayout [out]

Type: <b><a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout</a>**</b>

A pointer to the input-layout object created (see <a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout Interface</a>). To validate the other input parameters, set this pointer to be <b>NULL</b> and verify that the method returns S_FALSE.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a> for failing error codes.




## -remarks



After creating an input layout object, it must be bound to the input-assembler stage before calling a draw API. See <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">Getting Started with the Input-Assembler Stage (Direct3D 10)</a> for example code.

Once an input-layout object is created from a shader signature, the input-layout object can be reused with any other shader that has an identical input signature (semantics included). This can simplify the creation of input-layout objects when you are working with many shaders with identical inputs.

If a data type in the input-layout declaration does not match the data type in a shader-input signature, CreateInputLayout will generate a warning during compilation. The warning is simply to call attention to the fact that the data may be reinterpreted when read from a register. You may either disregard this warning (if reinterpretation is intentional) or make the data types match in both declarations to eliminate the warning.  The <a href="https://msdn.microsoft.com/454d3fd0-fc0f-46a9-925e-13f8e3c39f02">Data Conversion Rules</a> overview describes the rules applied for data type conversion.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Mapping the vertex data to the shader inputs with an input layout is a new way of doing things in Direct3D 10 that improves performance.

In Direct3D 10 the vertex data is mapped to the shader inputs when the input layout object is created, whereas in Direct3D 9 this mapping was done at Draw time based on the currently bound vertex declarations, vertex buffers, and vertex shaders. Doing this mapping when the input layout object is created reduces or eliminates extra linkage work for drivers at Draw time because this re-mapping is no longer necessary.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

