---
UID: NF:d3d10effect.ID3D10Effect.GetTechniqueByName
title: ID3D10Effect::GetTechniqueByName (d3d10effect.h)
author: windows-sdk-content
description: Get a technique by name.
old-location: direct3d10\id3d10effect_gettechniquebyname.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_gettechniquebyname.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 85db30ea-1e49-0b62-caca-5e0cf8959361, GetTechniqueByName, GetTechniqueByName method [Direct3D 10], GetTechniqueByName method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetTechniqueByName method, ID3D10Effect.GetTechniqueByName, ID3D10Effect::GetTechniqueByName, d3d10effect/ID3D10Effect::GetTechniqueByName, direct3d10.id3d10effect_gettechniquebyname
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
 - ID3D10Effect.GetTechniqueByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Effect::GetTechniqueByName


## -description


Get a technique by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the technique.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173708(v=VS.85).aspx">ID3D10EffectTechnique</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173708(v=VS.85).aspx">ID3D10EffectTechnique Interface</a>, or <b>NULL</b> if the technique is not found.




## -remarks



An effect contains one or more techniques; each technique contains one or more passes. You can access a technique using its name or with an index. For more about techniques, see <a href="https://msdn.microsoft.com/en-us/library/Bb205112(v=VS.85).aspx">techniques and passes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>
 

 

