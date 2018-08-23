---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetConstantBufferByName
title: ID3D11FunctionReflection::GetConstantBufferByName
author: windows-sdk-content
description: Gets a constant buffer by name for a function.
old-location: direct3d11\id3d11functionreflection_getconstantbufferbyname.htm
old-project: direct3d11
ms.assetid: 6629A13D-4D0A-4394-9D72-F786235BEA8E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 11], GetConstantBufferByName method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetConstantBufferByName method, ID3D11FunctionReflection.GetConstantBufferByName, ID3D11FunctionReflection::GetConstantBufferByName, d3d11shader/ID3D11FunctionReflection::GetConstantBufferByName, direct3d11.id3d11functionreflection_getconstantbufferbyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11shader.h
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
req.typenames: D3D11_SHADER_VERSION_TYPE
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11FunctionReflection::GetConstantBufferByName


## -description


Gets a constant buffer by name for a function.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476591(v=VS.85).aspx">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Ff476591(v=VS.85).aspx">ID3D11ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280546(v=VS.85).aspx">ID3D11FunctionReflection</a>
 

 

