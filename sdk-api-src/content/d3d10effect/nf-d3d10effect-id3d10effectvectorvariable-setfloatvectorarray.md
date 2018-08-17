---
UID: NF:d3d10effect.ID3D10EffectVectorVariable.SetFloatVectorArray
title: ID3D10EffectVectorVariable::SetFloatVectorArray
author: windows-sdk-content
description: Set an array of four-component vectors that contain floating-point data.
old-location: direct3d10\id3d10effectvectorvariable_setfloatvectorarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvectorvariable_setfloatvectorarray.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 9eb5f7ae-71eb-f3ae-ea6e-cc78dd935434, ID3D10EffectVectorVariable interface [Direct3D 10],SetFloatVectorArray method, ID3D10EffectVectorVariable.SetFloatVectorArray, ID3D10EffectVectorVariable::SetFloatVectorArray, SetFloatVectorArray, SetFloatVectorArray method [Direct3D 10], SetFloatVectorArray method [Direct3D 10],ID3D10EffectVectorVariable interface, d3d10effect/ID3D10EffectVectorVariable::SetFloatVectorArray, direct3d10.id3d10effectvectorvariable_setfloatvectorarray
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
 - ID3D10EffectVectorVariable.SetFloatVectorArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVectorVariable::SetFloatVectorArray


## -description


Set an array of four-component vectors that contain floating-point data.


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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bb8d5bb-5fc2-4fb2-aaf8-e8f01599e16d">ID3D10EffectVectorVariable Interface</a>
 

 

