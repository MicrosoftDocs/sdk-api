---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetResourceBindingDescByName
title: ID3D12ShaderReflection::GetResourceBindingDescByName
author: windows-sdk-content
description: Gets a description of how a resource is bound to a shader.
old-location: direct3d12\id3d12shaderreflection_getresourcebindingdescbyname.htm
old-project: direct3d12
ms.assetid: AA0FD49A-C5A2-4734-BDD6-FD739E4F5D59
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetResourceBindingDescByName, GetResourceBindingDescByName method, GetResourceBindingDescByName method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetResourceBindingDescByName method, ID3D12ShaderReflection.GetResourceBindingDescByName, ID3D12ShaderReflection::GetResourceBindingDescByName, d3d12shader/ID3D12ShaderReflection::GetResourceBindingDescByName, direct3d12.id3d12shaderreflection_getresourcebindingdescbyname
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D12ShaderReflection.GetResourceBindingDescByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflection::GetResourceBindingDescByName


## -description



          Gets a description of how a resource is bound to a shader.
        


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>


            The constant-buffer name of the resource.
          


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/4179C417-388D-4A20-8878-D074E20A706F">D3D12_SHADER_INPUT_BIND_DESC</a>*</b>


            A pointer to an input-binding description. See <a href="https://msdn.microsoft.com/4179C417-388D-4A20-8878-D074E20A706F">D3D12_SHADER_INPUT_BIND_DESC</a>.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




        A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDescByName</b> gets information about how one resource in the set is bound as an input to the shader. The  <i>Name</i> parameter specifies the name of the resource.
      


        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

