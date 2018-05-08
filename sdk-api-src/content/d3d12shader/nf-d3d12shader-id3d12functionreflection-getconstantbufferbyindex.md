---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetConstantBufferByIndex
title: ID3D12FunctionReflection::GetConstantBufferByIndex
author: windows-driver-content
description: Gets a constant buffer by index for a function.
old-location: direct3d12\id3d12functionreflection_getconstantbufferbyindex.htm
old-project: direct3d12
ms.assetid: 4B953072-DEF0-4A30-93A1-247B0C2CAFA3
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method, GetConstantBufferByIndex method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetConstantBufferByIndex method, ID3D12FunctionReflection.GetConstantBufferByIndex, ID3D12FunctionReflection::GetConstantBufferByIndex, d3d12shader/ID3D12FunctionReflection::GetConstantBufferByIndex, direct3d12.id3d12functionreflection_getconstantbufferbyindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12shader.h
api_name:
-	ID3D12FunctionReflection.GetConstantBufferByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12FunctionReflection::GetConstantBufferByIndex


## -description


Gets a constant buffer by index for a function.


## -parameters




### -param BufferIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.
          




## -remarks




        A constant buffer supplies either scalar constants or texture constants to a shader.
        A shader can use one or more constant buffers.
        For best performance, separate constants into buffers based on the frequency they are updated.
      




## -see-also




<a href="https://msdn.microsoft.com/F0BF4AA9-66D7-4A33-A51C-B03C1D61F537">ID3D12FunctionReflection</a>
 

 

