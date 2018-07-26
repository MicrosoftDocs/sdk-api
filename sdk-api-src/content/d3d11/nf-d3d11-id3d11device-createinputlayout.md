---
UID: NF:d3d11.ID3D11Device.CreateInputLayout
title: ID3D11Device::CreateInputLayout
author: windows-sdk-content
description: Create an input-layout object to describe the input-buffer data for the input-assembler stage.
old-location: direct3d11\id3d11device_createinputlayout.htm
old-project: direct3d11
ms.assetid: fe233b7b-3729-428a-8611-e98ea4c5af35
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 7e1008d3-1c16-4b6f-6b61-949b59c5f6d2, CreateInputLayout, CreateInputLayout method [Direct3D 11], CreateInputLayout method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateInputLayout method, ID3D11Device.CreateInputLayout, ID3D11Device::CreateInputLayout, d3d11/ID3D11Device::CreateInputLayout, direct3d11.id3d11device_createinputlayout
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateInputLayout
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateInputLayout


## -description


Create an input-layout object to describe the input-buffer data for the input-assembler stage.


## -parameters




### -param pInputElementDescs [in]

Type: <b>const <a href="https://msdn.microsoft.com/45545d24-1513-4efd-9344-20673c5b98d5">D3D11_INPUT_ELEMENT_DESC</a>*</b>

An array of the input-assembler stage input data types; each type is described by an element description (see <a href="https://msdn.microsoft.com/45545d24-1513-4efd-9344-20673c5b98d5">D3D11_INPUT_ELEMENT_DESC</a>).
          


### -param NumElements [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of input-data types in the array of input-elements.


### -param pShaderBytecodeWithInputSignature [in]

Type: <b>const void*</b>

A pointer to the compiled shader.  The compiled shader code contains a input signature which is validated against the array of elements. See remarks.
          


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled shader.


### -param ppInputLayout [out, optional]

Type: <b><a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>**</b>

A pointer to the input-layout object created (see <a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>). To validate the other input parameters, set this pointer to be <b>NULL</b> and verify that the method returns S_FALSE.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return code is S_OK. See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for failing error codes.
          




## -remarks



After creating an input layout object, it must be bound to the input-assembler stage before calling a draw API.

Once an input-layout object is created from a shader signature, the input-layout object can be reused with any other shader that has an identical input signature (semantics included). This can simplify the creation of input-layout objects when you are working with many shaders with identical inputs.

If a data type in the input-layout declaration does not match the data type in a shader-input signature, CreateInputLayout will generate a warning during compilation. The warning is simply to call attention to the fact that the data may be reinterpreted when read from a register. You may either disregard this warning (if reinterpretation is intentional) or make the data types match in both declarations to eliminate the warning.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

