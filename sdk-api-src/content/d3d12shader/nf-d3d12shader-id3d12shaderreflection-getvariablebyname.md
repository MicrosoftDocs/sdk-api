---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetVariableByName
title: ID3D12ShaderReflection::GetVariableByName
author: windows-sdk-content
description: Gets a variable by name.
old-location: direct3d12\id3d12shaderreflection_getvariablebyname.htm
old-project: direct3d12
ms.assetid: E79DACF1-2C89-42BB-BB04-DFA8280987C7
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetVariableByName, GetVariableByName method, GetVariableByName method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetVariableByName method, ID3D12ShaderReflection.GetVariableByName, ID3D12ShaderReflection::GetVariableByName, d3d12shader/ID3D12ShaderReflection::GetVariableByName, direct3d12.id3d12shaderreflection_getvariablebyname
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
 - ID3D12ShaderReflection.GetVariableByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflection::GetVariableByName


## -description



          Gets a variable by name.
        


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>


            A pointer to a string containing the variable name.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>*</b>


            Returns a <a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable Interface</a> interface.
          




## -remarks




        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

