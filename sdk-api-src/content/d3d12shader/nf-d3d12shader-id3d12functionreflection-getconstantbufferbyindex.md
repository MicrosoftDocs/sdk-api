---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetConstantBufferByIndex
title: ID3D12FunctionReflection::GetConstantBufferByIndex (d3d12shader.h)
author: windows-sdk-content
description: Gets a constant buffer by index for a function.
old-location: direct3d12\id3d12functionreflection_getconstantbufferbyindex.htm
tech.root: direct3d12
ms.assetid: 4B953072-DEF0-4A30-93A1-247B0C2CAFA3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method, GetConstantBufferByIndex method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetConstantBufferByIndex method, ID3D12FunctionReflection.GetConstantBufferByIndex, ID3D12FunctionReflection::GetConstantBufferByIndex, d3d12shader/ID3D12FunctionReflection::GetConstantBufferByIndex, direct3d12.id3d12functionreflection_getconstantbufferbyindex
ms.topic: method
f1_keywords: 
 - "d3d12shader/ID3D12FunctionReflection.GetConstantBufferByIndex"
dev_langs:
 - c++
req.header: d3d12shader.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12FunctionReflection.GetConstantBufferByIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12FunctionReflection::GetConstantBufferByIndex


## -description


Gets a constant buffer by index for a function.


## -parameters




### -param BufferIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer">ID3D12ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.
          




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader.
        A shader can use one or more constant buffers.
        For best performance, separate constants into buffers based on the frequency they are updated.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection">ID3D12FunctionReflection</a>
 

 

