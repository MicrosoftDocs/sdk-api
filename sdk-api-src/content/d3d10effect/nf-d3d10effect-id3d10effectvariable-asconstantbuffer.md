---
UID: NF:d3d10effect.ID3D10EffectVariable.AsConstantBuffer
title: ID3D10EffectVariable::AsConstantBuffer (d3d10effect.h)
author: windows-sdk-content
description: Get a constant buffer.
old-location: direct3d10\id3d10effectvariable_asconstantbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asconstantbuffer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 477c624a-b604-228f-bba0-0e26ed2d49e1, AsConstantBuffer, AsConstantBuffer method [Direct3D 10], AsConstantBuffer method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsConstantBuffer method, ID3D10EffectVariable.AsConstantBuffer, ID3D10EffectVariable::AsConstantBuffer, d3d10effect/ID3D10EffectVariable::AsConstantBuffer, direct3d10.id3d10effectvariable_asconstantbuffer
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
 - ID3D10EffectVariable.AsConstantBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable::AsConstantBuffer


## -description


Get a constant buffer.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173634(v=VS.85).aspx">ID3D10EffectConstantBuffer</a>*</b>

A pointer to a constant buffer. See <a href="https://msdn.microsoft.com/en-us/library/Bb173634(v=VS.85).aspx">ID3D10EffectConstantBuffer</a>.




## -remarks



AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

