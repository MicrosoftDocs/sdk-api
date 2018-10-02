---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetConstantBufferByName
title: ID3D11ShaderReflection::GetConstantBufferByName
author: windows-sdk-content
description: Get a constant buffer by name.
old-location: direct3d11\id3d11shaderreflection_getconstantbufferbyname.htm
tech.root: direct3d11
ms.assetid: 6b0e16c9-f45a-42d0-bd96-32dfa859b35d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 11], GetConstantBufferByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetConstantBufferByName method, ID3D11ShaderReflection.GetConstantBufferByName, ID3D11ShaderReflection::GetConstantBufferByName, d3d11shader/ID3D11ShaderReflection::GetConstantBufferByName, d50e9f46-8347-fa35-807d-0bbcf91adf69, direct3d11.id3d11shaderreflection_getconstantbufferbyname
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
 - ID3D11ShaderReflection.GetConstantBufferByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflection::GetConstantBufferByName


## -description


Get a constant buffer by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476591(v=VS.85).aspx">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="https://msdn.microsoft.com/en-us/library/Ff476591(v=VS.85).aspx">ID3D11ShaderReflectionConstantBuffer Interface</a>).




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476590(v=VS.85).aspx">ID3D11ShaderReflection Interface</a>
 

 

