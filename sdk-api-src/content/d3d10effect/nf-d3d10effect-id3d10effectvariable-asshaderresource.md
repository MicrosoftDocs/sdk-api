---
UID: NF:d3d10effect.ID3D10EffectVariable.AsShaderResource
title: ID3D10EffectVariable::AsShaderResource
author: windows-sdk-content
description: Get a shader-resource variable.
old-location: direct3d10\id3d10effectvariable_asshaderresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asshaderresource.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 9ecc402e-7c27-c872-6635-599b5c000326, AsShaderResource, AsShaderResource method [Direct3D 10], AsShaderResource method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsShaderResource method, ID3D10EffectVariable.AsShaderResource, ID3D10EffectVariable::AsShaderResource, d3d10effect/ID3D10EffectVariable::AsShaderResource, direct3d10.id3d10effectvariable_asshaderresource
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
 - ID3D10EffectVariable.AsShaderResource
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
- ID3D10EffectVariable.AsShaderResource
: 
---

# ID3D10EffectVariable::AsShaderResource


## -description


Get a shader-resource variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173693(v=VS.85).aspx">ID3D10EffectShaderResourceVariable</a>*</b>

A pointer to a shader-resource variable. See <a href="https://msdn.microsoft.com/en-us/library/Bb173693(v=VS.85).aspx">ID3D10EffectShaderResourceVariable</a>.




## -remarks



AsShaderResource returns a version of the effect variable that has been specialized to a shader-resource variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader-resource data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

