---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetConstantBufferByName
title: ID3D11FunctionReflection::GetConstantBufferByName
author: windows-sdk-content
description: Gets a constant buffer by name for a function.
old-location: direct3d11\id3d11functionreflection_getconstantbufferbyname.htm
tech.root: direct3d11
ms.assetid: 6629A13D-4D0A-4394-9D72-F786235BEA8E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 11], GetConstantBufferByName method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetConstantBufferByName method, ID3D11FunctionReflection.GetConstantBufferByName, ID3D11FunctionReflection::GetConstantBufferByName, d3d11shader/ID3D11FunctionReflection::GetConstantBufferByName, direct3d11.id3d11functionreflection_getconstantbufferbyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11FunctionReflection.GetConstantBufferByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11FunctionReflection::GetConstantBufferByName


## -description


Gets a constant buffer by name for a function.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://msdn.microsoft.com/91A3B6E3-E1A7-43F9-AD18-93A25F13CFB4">ID3D11FunctionReflection</a>
 

 

