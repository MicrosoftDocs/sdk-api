---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetConstantBufferByIndex
title: ID3D12ShaderReflection::GetConstantBufferByIndex
author: windows-sdk-content
description: Gets a constant buffer by index.
old-location: direct3d12\id3d12shaderreflection_getconstantbufferbyindex.htm
old-project: direct3d12
ms.assetid: 84E3240C-D21F-4F71-9AC2-C89570571A72
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetConstantBufferByIndex, GetConstantBufferByIndex method, GetConstantBufferByIndex method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetConstantBufferByIndex method, ID3D12ShaderReflection.GetConstantBufferByIndex, ID3D12ShaderReflection::GetConstantBufferByIndex, d3d12shader/ID3D12ShaderReflection::GetConstantBufferByIndex, direct3d12.id3d12shaderreflection_getconstantbufferbyindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12shader.h
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
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection.GetConstantBufferByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflection::GetConstantBufferByIndex


## -description


Gets a constant buffer by index.
        


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer Interface</a>).
          




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader. A shader can use one or more constant buffers. For best performance, separate constants into buffers based on the frequency they are updated.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

