---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetConstantBufferByName
title: ID3D12FunctionReflection::GetConstantBufferByName
author: windows-sdk-content
description: Gets a constant buffer by name for a function.
old-location: direct3d12\id3d12functionreflection_getconstantbufferbyname.htm
tech.root: direct3d12
ms.assetid: AB781E44-2FCE-4E20-955C-C6F9F6F3064B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method, GetConstantBufferByName method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetConstantBufferByName method, ID3D12FunctionReflection.GetConstantBufferByName, ID3D12FunctionReflection::GetConstantBufferByName, d3d12shader/ID3D12FunctionReflection::GetConstantBufferByName, direct3d12.id3d12functionreflection_getconstantbufferbyname
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
 - ID3D12FunctionReflection.GetConstantBufferByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12FunctionReflection::GetConstantBufferByName


## -description


Gets a constant buffer by name for a function.
        


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a> interface that represents the constant buffer.
          




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.
      




## -see-also




<a href="https://msdn.microsoft.com/F0BF4AA9-66D7-4A33-A51C-B03C1D61F537">ID3D12FunctionReflection</a>
 

 

