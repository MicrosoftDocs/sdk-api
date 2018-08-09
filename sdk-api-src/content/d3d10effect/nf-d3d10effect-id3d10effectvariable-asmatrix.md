---
UID: NF:d3d10effect.ID3D10EffectVariable.AsMatrix
title: ID3D10EffectVariable::AsMatrix
author: windows-sdk-content
description: Get a matrix variable.
old-location: direct3d10\id3d10effectvariable_asmatrix.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_asmatrix.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AsMatrix, AsMatrix method [Direct3D 10], AsMatrix method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],AsMatrix method, ID3D10EffectVariable.AsMatrix, ID3D10EffectVariable::AsMatrix, d3d10effect/ID3D10EffectVariable::AsMatrix, dc6784cd-b78e-6390-1d7a-db0d3c27410b, direct3d10.id3d10effectvariable_asmatrix
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
 - ID3D10EffectVariable.AsMatrix
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::AsMatrix


## -description


Get a matrix variable.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/82ffcc6e-9a92-4d72-a397-0a66600ad508">ID3D10EffectMatrixVariable</a>*</b>

A pointer to a matrix variable. See <a href="https://msdn.microsoft.com/82ffcc6e-9a92-4d72-a397-0a66600ad508">ID3D10EffectMatrixVariable</a>.




## -remarks



AsMatrix returns a version of the effect variable that has been specialized to a matrix variable. Similar to a cast, this specialization will return an invalid object if the effect variable does not contain matrix data.

Applications can test the returned object for validity by calling <a href="https://msdn.microsoft.com/b27f1669-94a1-4971-bd8f-e5a56f43560f">IsValid</a>.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

