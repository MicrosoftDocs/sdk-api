---
UID: NF:d3d10effect.ID3D10Effect.GetVariableByIndex
title: ID3D10Effect::GetVariableByIndex
author: windows-sdk-content
description: Get a variable by index.
old-location: direct3d10\id3d10effect_getvariablebyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebyindex.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 2e86399d-6be5-f4d4-507f-83c86d62cf4d, GetVariableByIndex, GetVariableByIndex method [Direct3D 10], GetVariableByIndex method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableByIndex method, ID3D10Effect.GetVariableByIndex, ID3D10Effect::GetVariableByIndex, d3d10effect/ID3D10Effect::GetVariableByIndex, direct3d10.id3d10effect_getvariablebyindex
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
 - ID3D10Effect.GetVariableByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10effect.h
: 
- ID3D10Effect.GetVariableByIndex
: 
---

# ID3D10Effect::GetVariableByIndex


## -description


Get a variable by index.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>.




## -remarks



An effect may contain one or more variables. Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique. You can access any local non-static effect variable using its name or with an index.

The method returns a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">effect-variable interface</a> if a variable is not found; you can call <a href="https://msdn.microsoft.com/en-us/library/Bb173772(v=VS.85).aspx">ID3D10Effect::IsValid</a> to verify whether or not the index exists.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>
 

 

