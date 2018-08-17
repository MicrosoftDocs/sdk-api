---
UID: NF:d3d10effect.ID3D10EffectVariable.AsDepthStencilView
title: ID3D10EffectVariable::AsDepthStencilView
author: windows-sdk-content
description: Get a depth-stencil-view variable.
old-location: direct3d10\id3d10effectvariable_asdepthstencilview.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asdepthstencilview.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AsDepthStencilView, AsDepthStencilView method [Direct3D 10], AsDepthStencilView method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsDepthStencilView method, ID3D10EffectVariable.AsDepthStencilView, ID3D10EffectVariable::AsDepthStencilView, cdd98874-51c7-7e0f-20f6-4efe28164ae0, d3d10effect/ID3D10EffectVariable::AsDepthStencilView, direct3d10.id3d10effectvariable_asdepthstencilview
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
 - ID3D10EffectVariable.AsDepthStencilView
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsDepthStencilView


## -description


Get a depth-stencil-view variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173642(v=VS.85).aspx">ID3D10EffectDepthStencilViewVariable</a>*</b>

A pointer to a depth-stencil-view variable. See <a href="https://msdn.microsoft.com/en-us/library/Bb173642(v=VS.85).aspx">ID3D10EffectDepthStencilViewVariable Interface</a>.




## -remarks



This method returns a version of the effect variable that has been specialized to a depth-stencil-view variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil-view data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

