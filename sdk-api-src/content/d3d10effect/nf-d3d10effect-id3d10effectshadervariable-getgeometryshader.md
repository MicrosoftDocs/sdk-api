---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetGeometryShader
title: ID3D10EffectShaderVariable::GetGeometryShader method
author: windows-driver-content
description: Get a geometry shader.
old-location: direct3d10\id3d10effectshadervariable_getgeometryshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getgeometryshader.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 3ec86a63-120a-f1df-c229-bbdd165c6650, GetGeometryShader method [Direct3D 10], GetGeometryShader method [Direct3D 10], ID3D10EffectShaderVariable interface, GetGeometryShader,ID3D10EffectShaderVariable.GetGeometryShader, ID3D10EffectShaderVariable, ID3D10EffectShaderVariable interface [Direct3D 10], GetGeometryShader method, ID3D10EffectShaderVariable::GetGeometryShader, d3d10effect/ID3D10EffectShaderVariable::GetGeometryShader, direct3d10.id3d10effectshadervariable_getgeometryshader
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectShaderVariable.GetGeometryShader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectShaderVariable::GetGeometryShader method


## -description


Get a geometry shader.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index.


### -param ppGS [out]

Type: <b><a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader</a>**</b>

A pointer to a <a href="https://msdn.microsoft.com/ffe713b9-93d6-4e0a-9cf6-014ac6b8a692">ID3D10GeometryShader Interface</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/636a0b4f-591a-467c-92e9-1b3d279465bb">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://msdn.microsoft.com/eeb1d34c-292a-4d35-9c3e-dc05b04f7913">ID3D10EffectShaderVariable</a>
 

 

