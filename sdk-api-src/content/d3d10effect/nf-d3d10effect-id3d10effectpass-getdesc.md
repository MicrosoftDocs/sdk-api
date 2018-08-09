---
UID: NF:d3d10effect.ID3D10EffectPass.GetDesc
title: ID3D10EffectPass::GetDesc
author: windows-sdk-content
description: Get a pass description.
old-location: direct3d10\id3d10effectpass_getdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getdesc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetDesc method, ID3D10EffectPass.GetDesc, ID3D10EffectPass::GetDesc, d144db62-661e-4008-27bf-01ee2d40f810, d3d10effect/ID3D10EffectPass::GetDesc, direct3d10.id3d10effectpass_getdesc
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
 - ID3D10EffectPass.GetDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectPass::GetDesc


## -description


Get a pass description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205330(v=VS.85).aspx">D3D10_PASS_DESC</a>*</b>

A pointer to a pass description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205330(v=VS.85).aspx">D3D10_PASS_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures). An effect technique contains one or more passes. See <a href="https://msdn.microsoft.com/en-us/library/Bb205112(v=VS.85).aspx">techniques and passes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass</a>
 

 

