---
UID: NF:d3d12shader.ID3D12ShaderReflectionVariable.GetDesc
title: ID3D12ShaderReflectionVariable::GetDesc
author: windows-sdk-content
description: Gets a shader-variable description.
old-location: direct3d12\id3d12shaderreflectionvariable_getdesc.htm
old-project: direct3d12
ms.assetid: 21CF98AF-5645-4059-992A-FFF778576C93
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetDesc, GetDesc method, GetDesc method,ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,GetDesc method, ID3D12ShaderReflectionVariable.GetDesc, ID3D12ShaderReflectionVariable::GetDesc, d3d12shader/ID3D12ShaderReflectionVariable::GetDesc, direct3d12.id3d12shaderreflectionvariable_getdesc
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
 - ID3D12ShaderReflectionVariable.GetDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionVariable::GetDesc


## -description


Gets a shader-variable description.
        


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/117181AB-16F4-41D7-974D-E2C04FEE4FB1">D3D12_SHADER_VARIABLE_DESC</a>*</b>

A pointer to a shader-variable description (see <a href="https://msdn.microsoft.com/117181AB-16F4-41D7-974D-E2C04FEE4FB1">D3D12_SHADER_VARIABLE_DESC</a>).
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



This method can be used to determine if the <a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable Interface</a> is valid, the method returns <b>E_FAIL</b> when the variable is not valid.
        

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>
 

 

