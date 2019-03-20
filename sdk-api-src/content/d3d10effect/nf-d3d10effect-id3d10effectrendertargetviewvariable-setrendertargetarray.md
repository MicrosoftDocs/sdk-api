---
UID: NF:d3d10effect.ID3D10EffectRenderTargetViewVariable.SetRenderTargetArray
title: ID3D10EffectRenderTargetViewVariable::SetRenderTargetArray (d3d10effect.h)
author: windows-sdk-content
description: Set an array of render-targets.
old-location: direct3d10\id3d10effectrendertargetviewvariable_setrendertargetarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectrendertargetviewvariable_setrendertargetarray.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10EffectRenderTargetViewVariable interface [Direct3D 10],SetRenderTargetArray method, ID3D10EffectRenderTargetViewVariable.SetRenderTargetArray, ID3D10EffectRenderTargetViewVariable::SetRenderTargetArray, SetRenderTargetArray, SetRenderTargetArray method [Direct3D 10], SetRenderTargetArray method [Direct3D 10],ID3D10EffectRenderTargetViewVariable interface, a376af5c-f301-a40d-27a2-6baa3ac58c55, d3d10effect/ID3D10EffectRenderTargetViewVariable::SetRenderTargetArray, direct3d10.id3d10effectrendertargetviewvariable_setrendertargetarray
ms.topic: method
req.header: d3d10effect.h
req.include-header: D3d10
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
 - d3d10effect.h
api_name:
 - ID3D10EffectRenderTargetViewVariable.SetRenderTargetArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectRenderTargetViewVariable::SetRenderTargetArray


## -description


Set an array of render-targets.


## -parameters




### -param ppResources [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView</a>**</b>

Set an array of render-target-view interfaces. See <a href="https://msdn.microsoft.com/en-us/library/Bb173827(v=VS.85).aspx">ID3D10RenderTargetView Interface</a>.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The zero-based array index to store the first interface.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements in the array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173672(v=VS.85).aspx">ID3D10EffectRenderTargetViewVariable Interface</a>
 

 

