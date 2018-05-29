---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetShaderDesc
title: ID3D10EffectShaderVariable::GetShaderDesc
author: windows-sdk-content
description: Get a shader description.
old-location: direct3d10\id3d10effectshadervariable_getshaderdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getshaderdesc.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetShaderDesc, GetShaderDesc method [Direct3D 10], GetShaderDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetShaderDesc method, ID3D10EffectShaderVariable.GetShaderDesc, ID3D10EffectShaderVariable::GetShaderDesc, d3d10effect/ID3D10EffectShaderVariable::GetShaderDesc, direct3d10.id3d10effectshadervariable_getshaderdesc, eb630246-c382-1984-9a6c-712450dfdd06
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectShaderVariable.GetShaderDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectShaderVariable::GetShaderDesc


## -description


Get a shader description.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/e300a787-9314-4752-8509-117ee291e9c8">D3D10_EFFECT_SHADER_DESC</a>*</b>

A pointer to a shader description (see <a href="https://msdn.microsoft.com/e300a787-9314-4752-8509-117ee291e9c8">D3D10_EFFECT_SHADER_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/636a0b4f-591a-467c-92e9-1b3d279465bb">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://msdn.microsoft.com/eeb1d34c-292a-4d35-9c3e-dc05b04f7913">ID3D10EffectShaderVariable</a>
 

 

