---
UID: NF:d3d10effect.ID3D10EffectVectorVariable.GetFloatVectorArray
title: ID3D10EffectVectorVariable::GetFloatVectorArray
author: windows-sdk-content
description: Get an array of four-component vectors that contain floating-point data.
old-location: direct3d10\id3d10effectvectorvariable_getfloatvectorarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvectorvariable_getfloatvectorarray.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0c6374bb-9ea0-894f-8f00-4c6aa56619e1, GetFloatVectorArray, GetFloatVectorArray method [Direct3D 10], GetFloatVectorArray method [Direct3D 10],ID3D10EffectVectorVariable interface, ID3D10EffectVectorVariable interface [Direct3D 10],GetFloatVectorArray method, ID3D10EffectVectorVariable.GetFloatVectorArray, ID3D10EffectVectorVariable::GetFloatVectorArray, d3d10effect/ID3D10EffectVectorVariable::GetFloatVectorArray, direct3d10.id3d10effectvectorvariable_getfloatvectorarray
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
 - ID3D10EffectVectorVariable.GetFloatVectorArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVectorVariable::GetFloatVectorArray


## -description


Get an array of four-component vectors that contain floating-point data.


## -parameters




### -param pData [in]

Type: <b>float*</b>

A pointer to the start of the data to set.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Must be set to 0; this is reserved for future use. 


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of array elements to set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173748(v=VS.85).aspx">ID3D10EffectVectorVariable Interface</a>
 

 

