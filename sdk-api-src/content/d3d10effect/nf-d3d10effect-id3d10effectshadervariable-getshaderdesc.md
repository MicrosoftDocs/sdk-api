---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetShaderDesc
title: ID3D10EffectShaderVariable::GetShaderDesc
author: windows-sdk-content
description: Get a shader description.
old-location: direct3d10\id3d10effectshadervariable_getshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getshaderdesc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetShaderDesc, GetShaderDesc method [Direct3D 10], GetShaderDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetShaderDesc method, ID3D10EffectShaderVariable.GetShaderDesc, ID3D10EffectShaderVariable::GetShaderDesc, d3d10effect/ID3D10EffectShaderVariable::GetShaderDesc, direct3d10.id3d10effectshadervariable_getshaderdesc, eb630246-c382-1984-9a6c-712450dfdd06
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10effect.h
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
 - D3D10Effect.h
api_name:
 - ID3D10EffectShaderVariable.GetShaderDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectShaderVariable::GetShaderDesc


## -description


Get a shader description.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205051(v=VS.85).aspx">D3D10_EFFECT_SHADER_DESC</a>*</b>

A pointer to a shader description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205051(v=VS.85).aspx">D3D10_EFFECT_SHADER_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173693(v=VS.85).aspx">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173698(v=VS.85).aspx">ID3D10EffectShaderVariable</a>
 

 

