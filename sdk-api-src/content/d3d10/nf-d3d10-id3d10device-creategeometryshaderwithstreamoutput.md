---
UID: NF:d3d10.ID3D10Device.CreateGeometryShaderWithStreamOutput
title: ID3D10Device::CreateGeometryShaderWithStreamOutput
author: windows-sdk-content
description: Creates a geometry shader that can write to streaming output buffers.
old-location: direct3d10\id3d10device_creategeometryshaderwithstreamoutput.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_creategeometryshaderwithstreamoutput.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1ef110f5-f95f-ec17-1f56-6f491a0ffac4, CreateGeometryShaderWithStreamOutput, CreateGeometryShaderWithStreamOutput method [Direct3D 10], CreateGeometryShaderWithStreamOutput method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateGeometryShaderWithStreamOutput method, ID3D10Device.CreateGeometryShaderWithStreamOutput, ID3D10Device::CreateGeometryShaderWithStreamOutput, d3d10/ID3D10Device::CreateGeometryShaderWithStreamOutput, direct3d10.id3d10device_creategeometryshaderwithstreamoutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ID3D10Device.CreateGeometryShaderWithStreamOutput
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateGeometryShaderWithStreamOutput


## -description


Creates a geometry shader that can write to streaming output buffers.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled geometry shader for a standard geometry shader plus stream output. For info on how to get this pointer, see <a href="https://msdn.microsoft.com/en-us/library/Bb509703(v=VS.85).aspx">Getting a Pointer to a Compiled Shader</a>.

To create the stream output without using a geometry shader, pass a pointer to the output signature for the prior stage. To obtain this output signature, call the <a href="https://msdn.microsoft.com/en-us/library/Dd607331(v=VS.85).aspx">D3DGetOutputSignatureBlob</a> compiler function. You can also pass a pointer to the compiled <a href="direct3d11.d3d10_graphics_programming_guide_shader_stages">vertex shader</a> that is used in the prior stage. This compiled shader provides the output signature for the data.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled geometry shader.


### -param pSODeclaration [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172450(v=VS.85).aspx">D3D10_SO_DECLARATION_ENTRY</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172450(v=VS.85).aspx">D3D10_SO_DECLARATION_ENTRY</a> array. Cannot be <b>NULL</b> if <i>NumEntries</i>&gt; 0.


### -param NumEntries [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of entries in the array pointed to by <i>pSODeclaration</i>. Minimum 0, maximum 64.


### -param OutputStreamStride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size, in bytes, of each element in the array pointed to by <i>pSODeclaration</i>. This parameter is only used when the output slot is 0 for all entries in <i>pSODeclaration</i>.


### -param ppGeometryShader [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173774(v=VS.85).aspx">ID3D10GeometryShader</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173774(v=VS.85).aspx">ID3D10GeometryShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



For more info about using <b>CreateGeometryShaderWithStreamOutput</b>, see <a href="https://msdn.microsoft.com/en-us/library/Bb205122(v=VS.85).aspx">Create a Geometry-Shader Object with Stream Output</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

