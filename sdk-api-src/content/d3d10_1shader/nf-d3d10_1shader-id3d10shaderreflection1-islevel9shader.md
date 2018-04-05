---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.IsLevel9Shader
title: ID3D10ShaderReflection1::IsLevel9Shader method
author: windows-driver-content
description: Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.
old-location: direct3d10\id3d10shaderreflection1_islevel9shader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_islevel9shader.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D10ShaderReflection1, ID3D10ShaderReflection1 interface [Direct3D 10], IsLevel9Shader method, ID3D10ShaderReflection1::IsLevel9Shader, IsLevel9Shader method [Direct3D 10], IsLevel9Shader method [Direct3D 10], ID3D10ShaderReflection1 interface, IsLevel9Shader,ID3D10ShaderReflection1.IsLevel9Shader, d3d10_1shader/ID3D10ShaderReflection1::IsLevel9Shader, direct3d10.id3d10shaderreflection1_islevel9shader, eca068fc-c01b-15d4-2317-dbe4b6cf2b82
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
-	ID3D10ShaderReflection1.IsLevel9Shader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection1::IsLevel9Shader method


## -description


Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.


## -parameters




### -param pbLevel9Shader [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Pointer to a BOOL variable that will be set true if the shader was compiled in Direct3D 10 on Direct3D 9 mode; otherwise false.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/344a0bf2-3ad8-4c58-b4d8-de386fdfd1c2">ID3D10ShaderReflection1 Interface</a>
 

 

