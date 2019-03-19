---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetResourceBindingDescByName
title: ID3D10ShaderReflection1::GetResourceBindingDescByName (d3d10_1shader.h)
author: windows-sdk-content
description: Gets a resource binding description by name.
old-location: direct3d10\id3d10shaderreflection1_getresourcebindingdescbyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getresourcebindingdescbyname.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 60aed60b-4d08-95c5-668d-2320735171ec, GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 10], GetResourceBindingDescByName method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetResourceBindingDescByName method, ID3D10ShaderReflection1.GetResourceBindingDescByName, ID3D10ShaderReflection1::GetResourceBindingDescByName, d3d10_1shader/ID3D10ShaderReflection1::GetResourceBindingDescByName, direct3d10.id3d10shaderreflection1_getresourcebindingdescbyname
ms.topic: method
req.header: d3d10_1shader.h
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
 - D3D10_1Shader.h
api_name:
 - ID3D10ShaderReflection1.GetResourceBindingDescByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10ShaderReflection1::GetResourceBindingDescByName


## -description


Gets a resource binding description by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a>*</b>

A pointer to a string containing the variable name.


### -param pDesc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172433(v=VS.85).aspx">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172433(v=VS.85).aspx">D3D10_SHADER_INPUT_BIND_DESC</a> structure that will be populated with resource binding information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb694550(v=VS.85).aspx">ID3D10ShaderReflection1 Interface</a>
 

 

