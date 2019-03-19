---
UID: NF:d3d10effect.ID3D10EffectVariable.AsVector
title: ID3D10EffectVariable::AsVector (d3d10effect.h)
author: windows-sdk-content
description: Get a vector variable.
old-location: direct3d10\id3d10effectvariable_asvector.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asvector.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AsVector, AsVector method [Direct3D 10], AsVector method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsVector method, ID3D10EffectVariable.AsVector, ID3D10EffectVariable::AsVector, a5136c3d-204c-bce5-0022-ead9b334e840, d3d10effect/ID3D10EffectVariable::AsVector, direct3d10.id3d10effectvariable_asvector
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
 - ID3D10EffectVariable.AsVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable::AsVector


## -description


Get a vector variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173748(v=VS.85).aspx">ID3D10EffectVectorVariable</a>*</b>

A pointer to a vector variable. See <a href="https://msdn.microsoft.com/en-us/library/Bb173748(v=VS.85).aspx">ID3D10EffectVectorVariable</a>.




## -remarks



AsVector returns a version of the effect variable that has been specialized to a vector variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

