---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetConstantBufferByIndex
title: ID3D11FunctionReflection::GetConstantBufferByIndex method
author: windows-driver-content
description: Gets a constant buffer by index for a function.
old-location: direct3d11\id3d11functionreflection_getconstantbufferbyindex.htm
old-project: direct3d11
ms.assetid: AFA54153-E205-4E6F-B328-9EC0262F2A5C
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetConstantBufferByIndex method [Direct3D 11], GetConstantBufferByIndex method [Direct3D 11], ID3D11FunctionReflection interface, GetConstantBufferByIndex,ID3D11FunctionReflection.GetConstantBufferByIndex, ID3D11FunctionReflection, ID3D11FunctionReflection interface [Direct3D 11], GetConstantBufferByIndex method, ID3D11FunctionReflection::GetConstantBufferByIndex, d3d11shader/ID3D11FunctionReflection::GetConstantBufferByIndex, direct3d11.id3d11functionreflection_getconstantbufferbyindex
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler_47.dll
api_name:
-	ID3D11FunctionReflection.GetConstantBufferByIndex
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionReflection::GetConstantBufferByIndex method


## -description


Gets a constant buffer by index for a function.


## -parameters




### -param BufferIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4b47ed8d-e814-4a7b-bc8e-25a8b71200ce">ID3D11ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://msdn.microsoft.com/91A3B6E3-E1A7-43F9-AD18-93A25F13CFB4">ID3D11FunctionReflection</a>
 

 

