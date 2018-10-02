---
UID: NF:d3d10effect.ID3D10EffectType.GetDesc
title: ID3D10EffectType::GetDesc
author: windows-sdk-content
description: Get an effect-type description.
old-location: direct3d10\id3d10effecttype_getdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effecttype_getdesc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 9e64bfa1-7fde-b141-e176-3bdc98f92982, GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10EffectType interface, ID3D10EffectType interface [Direct3D 10],GetDesc method, ID3D10EffectType.GetDesc, ID3D10EffectType::GetDesc, d3d10effect/ID3D10EffectType::GetDesc, direct3d10.id3d10effecttype_getdesc
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
 - ID3D10EffectType.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectType::GetDesc


## -description


Get an effect-type description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205054(v=VS.85).aspx">D3D10_EFFECT_TYPE_DESC</a>*</b>

A pointer to an effect-type description. See <a href="https://msdn.microsoft.com/en-us/library/Bb205054(v=VS.85).aspx">D3D10_EFFECT_TYPE_DESC</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173716(v=VS.85).aspx">ID3D10EffectType Interface</a>
 

 

