---
UID: NF:d3d10effect.ID3D10EffectVariable.AsScalar
title: ID3D10EffectVariable::AsScalar method
author: windows-driver-content
description: Get a scalar variable.
old-location: direct3d10\id3d10effectvariable_asscalar.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asscalar.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 12ddda89-a649-ce2c-648b-278f711c1808, AsScalar method [Direct3D 10], AsScalar method [Direct3D 10], ID3D10EffectVariable interface, AsScalar,ID3D10EffectVariable.AsScalar, ID3D10EffectVariable, ID3D10EffectVariable interface [Direct3D 10], AsScalar method, ID3D10EffectVariable::AsScalar, d3d10effect/ID3D10EffectVariable::AsScalar, direct3d10.id3d10effectvariable_asscalar
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
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10Effect.h
api_name:
-	ID3D10EffectVariable.AsScalar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsScalar method


## -description


Get a scalar variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/1129c4ff-2ea7-4556-8601-4339da7e67d3">ID3D10EffectScalarVariable</a>*</b>

A pointer to a scalar variable. See <a href="https://msdn.microsoft.com/1129c4ff-2ea7-4556-8601-4339da7e67d3">ID3D10EffectScalarVariable</a>.




## -remarks



AsScalar returns a version of the effect variable that has been specialized to a scalar variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain scalar data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

