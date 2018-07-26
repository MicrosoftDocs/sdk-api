---
UID: NF:d3d10effect.ID3D10EffectVariable.AsScalar
title: ID3D10EffectVariable::AsScalar
author: windows-sdk-content
description: Get a scalar variable.
old-location: direct3d10\id3d10effectvariable_asscalar.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asscalar.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 12ddda89-a649-ce2c-648b-278f711c1808, AsScalar, AsScalar method [Direct3D 10], AsScalar method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsScalar method, ID3D10EffectVariable.AsScalar, ID3D10EffectVariable::AsScalar, d3d10effect/ID3D10EffectVariable::AsScalar, direct3d10.id3d10effectvariable_asscalar
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
 - ID3D10EffectVariable.AsScalar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsScalar


## -description


Get a scalar variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Bb173680(v=VS.85).aspx">ID3D10EffectScalarVariable</a>*</b>

A pointer to a scalar variable. See <a href="https://msdn.microsoft.com/library/Bb173680(v=VS.85).aspx">ID3D10EffectScalarVariable</a>.




## -remarks



AsScalar returns a version of the effect variable that has been specialized to a scalar variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain scalar data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/library/Bb173746(v=VS.85).aspx">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

