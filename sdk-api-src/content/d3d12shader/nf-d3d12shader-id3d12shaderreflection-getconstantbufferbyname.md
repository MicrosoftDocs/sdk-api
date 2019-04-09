---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetConstantBufferByName
title: ID3D12ShaderReflection::GetConstantBufferByName (d3d12shader.h)
author: windows-sdk-content
description: Gets a constant buffer by name.
old-location: direct3d12\id3d12shaderreflection_getconstantbufferbyname.htm
tech.root: direct3d12
ms.assetid: C8BE8C17-2B5A-45AB-8C39-778FFFA78992
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method, GetConstantBufferByName method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetConstantBufferByName method, ID3D12ShaderReflection.GetConstantBufferByName, ID3D12ShaderReflection::GetConstantBufferByName, d3d12shader/ID3D12ShaderReflection::GetConstantBufferByName, direct3d12.id3d12shaderreflection_getconstantbufferbyname
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
 - ID3D12ShaderReflection.GetConstantBufferByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflection::GetConstantBufferByName


## -description


Gets a constant buffer by name.
        


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>*</b>

A pointer to a constant buffer (see <a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer Interface</a>).
          




## -remarks



A constant buffer supplies either scalar constants or texture constants to a shader.
        A shader can use one or more constant buffers.
        For best performance, separate constants into buffers based on the frequency they are updated.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

