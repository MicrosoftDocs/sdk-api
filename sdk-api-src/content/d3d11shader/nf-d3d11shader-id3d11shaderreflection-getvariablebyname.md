---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetVariableByName
title: ID3D11ShaderReflection::GetVariableByName
author: windows-sdk-content
description: Gets a variable by name.
old-location: direct3d11\id3d11shaderreflection_getvariablebyname.htm
old-project: direct3d11
ms.assetid: 8c21756f-40f0-4459-852b-445053aa03e8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 714dbbf5-52e2-8540-c5c1-aa03dcf32bf2, GetVariableByName, GetVariableByName method [Direct3D 11], GetVariableByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetVariableByName method, ID3D11ShaderReflection.GetVariableByName, ID3D11ShaderReflection::GetVariableByName, d3d11shader/ID3D11ShaderReflection::GetVariableByName, direct3d11.id3d11shaderreflection_getvariablebyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11shader.h
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflection.GetVariableByName
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ShaderReflection::GetVariableByName


## -description


Gets a variable by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

A pointer to a string containing the variable name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476607(v=VS.85).aspx">ID3D11ShaderReflectionVariable</a>*</b>

Returns a <a href="https://msdn.microsoft.com/en-us/library/Ff476607(v=VS.85).aspx">ID3D11ShaderReflectionVariable Interface</a> interface.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476590(v=VS.85).aspx">ID3D11ShaderReflection Interface</a>
 

 

