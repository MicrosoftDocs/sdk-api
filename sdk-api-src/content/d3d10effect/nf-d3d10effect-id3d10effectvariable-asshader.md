---
UID: NF:d3d10effect.ID3D10EffectVariable.AsShader
title: ID3D10EffectVariable::AsShader
author: windows-sdk-content
description: Get a shader variable.
old-location: direct3d10\id3d10effectvariable_asshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asshader.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AsShader, AsShader method [Direct3D 10], AsShader method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsShader method, ID3D10EffectVariable.AsShader, ID3D10EffectVariable::AsShader, cfb94875-697a-f808-87e1-768dc74cc207, d3d10effect/ID3D10EffectVariable::AsShader, direct3d10.id3d10effectvariable_asshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectVariable.AsShader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsShader


## -description


Get a shader variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/eeb1d34c-292a-4d35-9c3e-dc05b04f7913">ID3D10EffectShaderVariable</a>*</b>

A pointer to a shader variable. See <a href="https://msdn.microsoft.com/eeb1d34c-292a-4d35-9c3e-dc05b04f7913">ID3D10EffectShaderVariable</a>.




## -remarks



AsShader returns a version of the effect variable that has been specialized to a shader variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

