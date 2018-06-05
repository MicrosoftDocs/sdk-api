---
UID: NS:d3d12shader._D3D12_SHADER_BUFFER_DESC
title: "_D3D12_SHADER_BUFFER_DESC"
author: windows-sdk-content
description: Describes a shader constant-buffer.
old-location: direct3d12\d3d12_shader_buffer_desc.htm
old-project: direct3d12
ms.assetid: 03F36467-9841-4385-9962-D7ADB4D79C6C
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_SHADER_BUFFER_DESC, D3D12_SHADER_BUFFER_DESC structure, _D3D12_SHADER_BUFFER_DESC, d3d12shader/D3D12_SHADER_BUFFER_DESC, direct3d12.d3d12_shader_buffer_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D12_SHADER_BUFFER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12shader.h
api_name:
-	D3D12_SHADER_BUFFER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D12_SHADER_BUFFER_DESC structure


## -description



          Describes a shader constant-buffer.
        


## -struct-fields




### -field Name


            The name of the buffer.
          


### -field Type


            A <a href="https://msdn.microsoft.com/b21a460b-63cb-49c1-bd6c-a747df495efc">D3D_CBUFFER_TYPE</a>-typed value that indicates the intended use of the constant data.
          


### -field Variables


            The number of unique variables.
          


### -field Size


            The size of the buffer, in bytes.
          


### -field uFlags


            A combination of <a href="https://msdn.microsoft.com/f641b3ec-5492-4835-9cf6-e41447e4b6b6">D3D_SHADER_CBUFFER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies properties for the shader constant-buffer.
          


## -remarks




        Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="https://msdn.microsoft.com/33D6926F-BF1B-4424-BC28-83F8A4A30589">ID3D12ShaderReflectionConstantBuffer::GetDesc</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0">Shader Structures</a>
 

 

