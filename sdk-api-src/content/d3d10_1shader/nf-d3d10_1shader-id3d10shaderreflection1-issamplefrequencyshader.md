---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.IsSampleFrequencyShader
title: ID3D10ShaderReflection1::IsSampleFrequencyShader
author: windows-sdk-content
description: Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.
old-location: direct3d10\id3d10shaderreflection1_issamplefrequencyshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_issamplefrequencyshader.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 97227f17-7b34-25ea-a5ce-d0eeaad6f201, ID3D10ShaderReflection1 interface [Direct3D 10],IsSampleFrequencyShader method, ID3D10ShaderReflection1.IsSampleFrequencyShader, ID3D10ShaderReflection1::IsSampleFrequencyShader, IsSampleFrequencyShader, IsSampleFrequencyShader method [Direct3D 10], IsSampleFrequencyShader method [Direct3D 10],ID3D10ShaderReflection1 interface, d3d10_1shader/ID3D10ShaderReflection1::IsSampleFrequencyShader, direct3d10.id3d10shaderreflection1_issamplefrequencyshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10_1shader.h
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
req.typenames: D3D10_SHADER_DEBUG_VARTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1Shader.h
api_name:
 - ID3D10ShaderReflection1.IsSampleFrequencyShader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10ShaderReflection1::IsSampleFrequencyShader


## -description


Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.


## -parameters




### -param pbSampleFrequency

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

A pointer to a BOOL variable that will be set to true if the shader is intended to run at sample frequency; false otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb694550(v=VS.85).aspx">ID3D10ShaderReflection1 Interface</a>
 

 

