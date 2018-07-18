---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.GetFloatArray
title: ID3D10EffectScalarVariable::GetFloatArray
author: windows-sdk-content
description: Get an array of floating-point variables.
old-location: direct3d10\id3d10effectscalarvariable_getfloatarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_getfloatarray.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetFloatArray, GetFloatArray method [Direct3D 10], GetFloatArray method [Direct3D 10],ID3D10EffectScalarVariable interface, ID3D10EffectScalarVariable interface [Direct3D 10],GetFloatArray method, ID3D10EffectScalarVariable.GetFloatArray, ID3D10EffectScalarVariable::GetFloatArray, d3d10effect/ID3D10EffectScalarVariable::GetFloatArray, direct3d10.id3d10effectscalarvariable_getfloatarray, e8606cb9-74af-2b45-f488-1115ae3ccba4
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
 - ID3D10EffectScalarVariable.GetFloatArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectScalarVariable::GetFloatArray


## -description


Get an array of floating-point variables.


## -parameters




### -param pData [out]

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




<a href="https://msdn.microsoft.com/1129c4ff-2ea7-4556-8601-4339da7e67d3">ID3D10EffectScalarVariable Interface</a>
 

 

