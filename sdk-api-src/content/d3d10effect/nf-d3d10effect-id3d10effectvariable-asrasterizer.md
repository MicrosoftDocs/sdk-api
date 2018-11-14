---
UID: NF:d3d10effect.ID3D10EffectVariable.AsRasterizer
title: ID3D10EffectVariable::AsRasterizer
author: windows-sdk-content
description: Get a rasterizer variable.
old-location: direct3d10\id3d10effectvariable_asrasterizer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asrasterizer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0306e054-b8c5-9b23-2bcb-82e72a683879, AsRasterizer, AsRasterizer method [Direct3D 10], AsRasterizer method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsRasterizer method, ID3D10EffectVariable.AsRasterizer, ID3D10EffectVariable::AsRasterizer, d3d10effect/ID3D10EffectVariable::AsRasterizer, direct3d10.id3d10effectvariable_asrasterizer
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
 - ID3D10EffectVariable.AsRasterizer
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
- ID3D10EffectVariable.AsRasterizer
: 
---

# ID3D10EffectVariable::AsRasterizer


## -description


Get a rasterizer variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173669(v=VS.85).aspx">ID3D10EffectRasterizerVariable</a>*</b>

A pointer to a rasterizer variable. See <a href="https://msdn.microsoft.com/en-us/library/Bb173669(v=VS.85).aspx">ID3D10EffectRasterizerVariable</a>.




## -remarks



AsRasterizer returns a version of the effect variable that has been specialized to a rasterizer variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain rasterizer data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

