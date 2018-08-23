---
UID: NF:d3d10effect.ID3D10EffectScalarVariable.SetBoolArray
title: ID3D10EffectScalarVariable::SetBoolArray
author: windows-sdk-content
description: Set an array of boolean variables.
old-location: direct3d10\id3d10effectscalarvariable_setboolarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectscalarvariable_setboolarray.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 596545fb-be65-5d46-6b19-d6fd77f59c4b, ID3D10EffectScalarVariable interface [Direct3D 10],SetBoolArray method, ID3D10EffectScalarVariable.SetBoolArray, ID3D10EffectScalarVariable::SetBoolArray, SetBoolArray, SetBoolArray method [Direct3D 10], SetBoolArray method [Direct3D 10],ID3D10EffectScalarVariable interface, d3d10effect/ID3D10EffectScalarVariable::SetBoolArray, direct3d10.id3d10effectscalarvariable_setboolarray
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
 - ID3D10EffectScalarVariable.SetBoolArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectScalarVariable::SetBoolArray


## -description


Set an array of boolean variables.


## -parameters




### -param pData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

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
 

 

