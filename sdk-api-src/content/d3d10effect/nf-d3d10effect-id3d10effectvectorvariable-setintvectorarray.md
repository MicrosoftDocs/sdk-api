---
UID: NF:d3d10effect.ID3D10EffectVectorVariable.SetIntVectorArray
title: ID3D10EffectVectorVariable::SetIntVectorArray
author: windows-sdk-content
description: Set an array of four-component vectors that contain integer data.
old-location: direct3d10\id3d10effectvectorvariable_setintvectorarray.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvectorvariable_setintvectorarray.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10EffectVectorVariable interface [Direct3D 10],SetIntVectorArray method, ID3D10EffectVectorVariable.SetIntVectorArray, ID3D10EffectVectorVariable::SetIntVectorArray, SetIntVectorArray, SetIntVectorArray method [Direct3D 10], SetIntVectorArray method [Direct3D 10],ID3D10EffectVectorVariable interface, c3a5fdc0-0b12-1092-5034-1af95e45a5cb, d3d10effect/ID3D10EffectVectorVariable::SetIntVectorArray, direct3d10.id3d10effectvectorvariable_setintvectorarray
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
 - ID3D10EffectVectorVariable.SetIntVectorArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVectorVariable::SetIntVectorArray


## -description


Set an array of four-component vectors that contain integer data.


## -parameters




### -param pData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">int</a>*</b>

A pointer to the start of the data to set.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Must be set to 0; this is reserved for future use. 


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of array elements to set.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bb8d5bb-5fc2-4fb2-aaf8-e8f01599e16d">ID3D10EffectVectorVariable Interface</a>
 

 

