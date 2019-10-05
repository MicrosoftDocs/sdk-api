---
UID: NF:d3d10_1shader.ID3D10ShaderReflection1.IsSampleFrequencyShader
title: ID3D10ShaderReflection1::IsSampleFrequencyShader (d3d10_1shader.h)
author: windows-sdk-content
description: Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.
old-location: direct3d10\id3d10shaderreflection1_issamplefrequencyshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection1_issamplefrequencyshader.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 97227f17-7b34-25ea-a5ce-d0eeaad6f201, ID3D10ShaderReflection1 interface [Direct3D 10],IsSampleFrequencyShader method, ID3D10ShaderReflection1.IsSampleFrequencyShader, ID3D10ShaderReflection1::IsSampleFrequencyShader, IsSampleFrequencyShader, IsSampleFrequencyShader method [Direct3D 10], IsSampleFrequencyShader method [Direct3D 10],ID3D10ShaderReflection1 interface, d3d10_1shader/ID3D10ShaderReflection1::IsSampleFrequencyShader, direct3d10.id3d10shaderreflection1_issamplefrequencyshader
ms.topic: method
f1_keywords: 
 - "d3d10_1shader/ID3D10ShaderReflection1.IsSampleFrequencyShader"
dev_langs:
 - c++
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
 - ID3D10ShaderReflection1.IsSampleFrequencyShader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10ShaderReflection1::IsSampleFrequencyShader


## -description


Indicates whether a pixel shader is intended to run a pixel frequency or sample frequency.


## -parameters




### -param pbSampleFrequency

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

A pointer to a BOOL variable that will be set to true if the shader is intended to run at sample frequency; false otherwise.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10_1shader/nn-d3d10_1shader-id3d10shaderreflection1">ID3D10ShaderReflection1 Interface</a>
 

 

