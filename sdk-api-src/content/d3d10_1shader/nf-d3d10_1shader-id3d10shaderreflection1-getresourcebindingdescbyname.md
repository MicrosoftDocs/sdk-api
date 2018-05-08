---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.GetResourceBindingDescByName
title: ID3D10ShaderReflection1::GetResourceBindingDescByName
author: windows-driver-content
description: Gets a resource binding description by name.
old-location: direct3d10\id3d10shaderreflection1_getresourcebindingdescbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_getresourcebindingdescbyname.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 60aed60b-4d08-95c5-668d-2320735171ec, GetResourceBindingDescByName, GetResourceBindingDescByName method [Direct3D 10], GetResourceBindingDescByName method [Direct3D 10],ID3D10ShaderReflection1 interface, ID3D10ShaderReflection1 interface [Direct3D 10],GetResourceBindingDescByName method, ID3D10ShaderReflection1.GetResourceBindingDescByName, ID3D10ShaderReflection1::GetResourceBindingDescByName, d3d10_1shader/ID3D10ShaderReflection1::GetResourceBindingDescByName, direct3d10.id3d10shaderreflection1_getresourcebindingdescbyname
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D10_SHADER_DEBUG_VARTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10_1Shader.h
api_name:
-	ID3D10ShaderReflection1.GetResourceBindingDescByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection1::GetResourceBindingDescByName


## -description


Gets a resource binding description by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a>*</b>

A pointer to a string containing the variable name.


### -param pDesc

Type: <b><a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8929f7d4-6fd0-4b48-b1d8-0b089d4c730d">D3D10_SHADER_INPUT_BIND_DESC</a> structure that will be populated with resource binding information.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/344a0bf2-3ad8-4c58-b4d8-de386fdfd1c2">ID3D10ShaderReflection1 Interface</a>
 

 

