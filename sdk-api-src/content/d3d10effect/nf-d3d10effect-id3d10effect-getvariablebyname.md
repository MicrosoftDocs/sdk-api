---
UID: NF:d3d10effect.ID3D10Effect.GetVariableByName
title: ID3D10Effect::GetVariableByName
author: windows-sdk-content
description: Get a variable by name.
old-location: direct3d10\id3d10effect_getvariablebyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebyname.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetVariableByName, GetVariableByName method [Direct3D 10], GetVariableByName method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableByName method, ID3D10Effect.GetVariableByName, ID3D10Effect::GetVariableByName, c08eacd5-3abc-89d5-a465-058f2f195794, d3d10effect/ID3D10Effect::GetVariableByName, direct3d10.id3d10effect_getvariablebyname
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
 - ID3D10Effect.GetVariableByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Effect::GetVariableByName


## -description


Get a variable by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The variable name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>.




## -remarks



An effect may contain one or more variables. Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique. You can access an effect variable using its name or with an index.

The method returns a pointer to an <a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">effect-variable interface</a> if a variable is not found; you can call <a href="https://msdn.microsoft.com/e31defc8-92cf-4409-bfe6-5e8e98c4e44f">ID3D10Effect::IsValid</a> to verify whether or not the name exists.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>
 

 

