---
UID: NF:d3d10effect.ID3D10Effect.GetVariableBySemantic
title: ID3D10Effect::GetVariableBySemantic
author: windows-sdk-content
description: Get a variable by semantic.
old-location: direct3d10\id3d10effect_getvariablebysemantic.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getvariablebysemantic.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetVariableBySemantic, GetVariableBySemantic method [Direct3D 10], GetVariableBySemantic method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetVariableBySemantic method, ID3D10Effect.GetVariableBySemantic, ID3D10Effect::GetVariableBySemantic, d3d10effect/ID3D10Effect::GetVariableBySemantic, direct3d10.id3d10effect_getvariablebysemantic, e578cd0d-594a-b43e-8baa-310f0b747079
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
 - ID3D10Effect.GetVariableBySemantic
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Effect::GetVariableBySemantic


## -description


Get a variable by semantic.


## -parameters




### -param Semantic [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The semantic name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable</a>*</b>

A pointer to the effect variable indicated by the Semantic. See <a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>.




## -remarks



Each effect variable can have a semantic attached, which is a user defined metadata string. Some <a href="https://msdn.microsoft.com/library/Bb509647(v=VS.85).aspx">system-value semantics</a> are reserved words that trigger built in functionality by pipeline stages.

The method returns a pointer to an <a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">effect-variable interface</a> if a variable is not found; you can call <a href="https://msdn.microsoft.com/library/Bb173772(v=VS.85).aspx">ID3D10Effect::IsValid</a> to verify whether or not the semantic exists.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>
 

 

