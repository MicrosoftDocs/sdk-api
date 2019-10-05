---
UID: NF:d3d11shader.ID3D11FunctionReflection.GetConstantBufferByIndex
title: ID3D11FunctionReflection::GetConstantBufferByIndex (d3d11shader.h)
author: windows-sdk-content
description: Gets a constant buffer by index for a function.
old-location: direct3d11\id3d11functionreflection_getconstantbufferbyindex.htm
tech.root: direct3d11
ms.assetid: AFA54153-E205-4E6F-B328-9EC0262F2A5C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method [Direct3D 11], GetConstantBufferByIndex method [Direct3D 11],ID3D11FunctionReflection interface, ID3D11FunctionReflection interface [Direct3D 11],GetConstantBufferByIndex method, ID3D11FunctionReflection.GetConstantBufferByIndex, ID3D11FunctionReflection::GetConstantBufferByIndex, d3d11shader/ID3D11FunctionReflection::GetConstantBufferByIndex, direct3d11.id3d11functionreflection_getconstantbufferbyindex
ms.topic: method
f1_keywords: 
 - "d3d11shader/ID3D11FunctionReflection.GetConstantBufferByIndex"
dev_langs:
 - c++
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
 - ID3D11FunctionReflection.GetConstantBufferByIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11FunctionReflection::GetConstantBufferByIndex


## -description


Gets a constant buffer by index for a function.


## -parameters




### -param BufferIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer">ID3D11ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionreflection">ID3D11FunctionReflection</a>
 

 

