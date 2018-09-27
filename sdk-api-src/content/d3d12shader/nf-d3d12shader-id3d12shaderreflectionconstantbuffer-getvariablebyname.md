---
UID: NF:d3d12shader.ID3D12ShaderReflectionConstantBuffer.GetVariableByName
title: ID3D12ShaderReflectionConstantBuffer::GetVariableByName
author: windows-sdk-content
description: Gets a shader-reflection variable by name.
old-location: direct3d12\id3d12shaderreflectionconstantbuffer_getvariablebyname.htm
tech.root: direct3d12
ms.assetid: FD18A64F-9B4A-42FE-8E18-13E9375E19BC
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetVariableByName, GetVariableByName method, GetVariableByName method,ID3D12ShaderReflectionConstantBuffer interface, ID3D12ShaderReflectionConstantBuffer interface,GetVariableByName method, ID3D12ShaderReflectionConstantBuffer.GetVariableByName, ID3D12ShaderReflectionConstantBuffer::GetVariableByName, d3d12shader/ID3D12ShaderReflectionConstantBuffer::GetVariableByName, direct3d12.id3d12shaderreflectionconstantbuffer_getvariablebyname
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
 - ID3D12ShaderReflectionConstantBuffer.GetVariableByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflectionConstantBuffer::GetVariableByName


## -description


Gets a shader-reflection variable by name.
        


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Variable name.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>*</b>

Returns a sentinel object (end of list marker). To determine if GetVariableByName successfully completed, call <a href="https://msdn.microsoft.com/21CF98AF-5645-4059-992A-FFF778576C93">ID3D12ShaderReflectionVariable::GetDesc</a> and check the returned <b>HRESULT</b>; any return value other than success means that GetVariableByName failed.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/4102AF77-3EC7-42CD-8B9C-6D0CC999529A">ID3D12ShaderReflectionConstantBuffer</a>
 

 

