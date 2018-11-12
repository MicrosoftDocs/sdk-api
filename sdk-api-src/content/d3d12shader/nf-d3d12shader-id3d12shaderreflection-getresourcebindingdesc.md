---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetResourceBindingDesc
title: ID3D12ShaderReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Gets a description of how a resource is bound to a shader.
old-location: direct3d12\id3d12shaderreflection_getresourcebindingdesc.htm
tech.root: direct3d12
ms.assetid: 3E9A168D-CD9E-4256-9E0B-19B9295E511E
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method, GetResourceBindingDesc method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetResourceBindingDesc method, ID3D12ShaderReflection.GetResourceBindingDesc, ID3D12ShaderReflection::GetResourceBindingDesc, d3d12shader/ID3D12ShaderReflection::GetResourceBindingDesc, direct3d12.id3d12shaderreflection_getresourcebindingdesc
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
 - ID3D12ShaderReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ShaderReflection::GetResourceBindingDesc


## -description


Gets a description of how a resource is bound to a shader.
        


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A zero-based resource index.
          


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn960201(v=VS.85).aspx">D3D12_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/en-us/library/Dn960201(v=VS.85).aspx">D3D12_SHADER_INPUT_BIND_DESC</a>.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets information about how one resource in the set is bound as an input to the shader. The  <i>ResourceIndex</i> parameter specifies the index for the resource.
      

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

