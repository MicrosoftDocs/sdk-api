---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.GetBoolArray
title: ID3D10EffectScalarVariable::GetBoolArray
author: windows-sdk-content
description: Get an array of boolean variables.
old-location: direct3d10\id3d10effectscalarvariable_getboolarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_getboolarray.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetBoolArray, GetBoolArray method [Direct3D 10], GetBoolArray method [Direct3D 10],ID3D10EffectScalarVariable interface, ID3D10EffectScalarVariable interface [Direct3D 10],GetBoolArray method, ID3D10EffectScalarVariable.GetBoolArray, ID3D10EffectScalarVariable::GetBoolArray, d3d10effect/ID3D10EffectScalarVariable::GetBoolArray, direct3d10.id3d10effectscalarvariable_getboolarray, fbddf130-1eef-5bad-8fad-819c89e5a371
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
 - ID3D10EffectScalarVariable.GetBoolArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectScalarVariable::GetBoolArray


## -description


Get an array of boolean variables.


## -parameters




### -param pData [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

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




<a href="https://msdn.microsoft.com/en-us/library/Bb173680(v=VS.85).aspx">ID3D10EffectScalarVariable Interface</a>
 

 

