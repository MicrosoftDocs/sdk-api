---
UID: NF:d3d10effect.ID3D10EffectVariable.AsDepthStencil
title: ID3D10EffectVariable::AsDepthStencil
author: windows-sdk-content
description: Get a depth-stencil variable.
old-location: direct3d10\id3d10effectvariable_asdepthstencil.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asdepthstencil.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: AsDepthStencil, AsDepthStencil method [Direct3D 10], AsDepthStencil method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsDepthStencil method, ID3D10EffectVariable.AsDepthStencil, ID3D10EffectVariable::AsDepthStencil, d12d55ad-aa27-e1e7-7fbd-f7bbe4c54754, d3d10effect/ID3D10EffectVariable::AsDepthStencil, direct3d10.id3d10effectvariable_asdepthstencil
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
 - ID3D10EffectVariable.AsDepthStencil
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsDepthStencil


## -description


Get a depth-stencil variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Bb173639(v=VS.85).aspx">ID3D10EffectDepthStencilVariable</a>*</b>

A pointer to a depth-stencil variable. See <a href="https://msdn.microsoft.com/library/Bb173639(v=VS.85).aspx">ID3D10EffectDepthStencilVariable</a>.




## -remarks



AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

