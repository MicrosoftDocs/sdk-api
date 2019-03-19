---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.IsLevel9Shader
title: ID3D10ShaderReflection1::IsLevel9Shader (d3d10_1shader.h)
author: windows-sdk-content
description: Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.
old-location: direct3d10\id3d10shaderreflection1_islevel9shader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_islevel9shader.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10ShaderReflection1 interface [Direct3D 10],IsLevel9Shader method, ID3D10ShaderReflection1.IsLevel9Shader, ID3D10ShaderReflection1::IsLevel9Shader, IsLevel9Shader, IsLevel9Shader method [Direct3D 10], IsLevel9Shader method [Direct3D 10],ID3D10ShaderReflection1 interface, d3d10_1shader/ID3D10ShaderReflection1::IsLevel9Shader, direct3d10.id3d10shaderreflection1_islevel9shader, eca068fc-c01b-15d4-2317-dbe4b6cf2b82
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
 - ID3D10ShaderReflection1.IsLevel9Shader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10ShaderReflection1::IsLevel9Shader


## -description


Indicates whether a shader was compiled in Direct3D 10 on Direct3D 9 mode.


## -parameters




### -param pbLevel9Shader [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Pointer to a BOOL variable that will be set true if the shader was compiled in Direct3D 10 on Direct3D 9 mode; otherwise false.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb694550(v=VS.85).aspx">ID3D10ShaderReflection1 Interface</a>
 

 

