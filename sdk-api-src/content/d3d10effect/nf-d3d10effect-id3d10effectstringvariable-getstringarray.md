---
UID: NF:d3d10effect.ID3D10EffectStringVariable.GetStringArray
title: ID3D10EffectStringVariable::GetStringArray method
author: windows-driver-content
description: Get an array of strings.
old-location: direct3d10\id3d10effectstringvariable_getstringarray.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectstringvariable_getstringarray.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 3a4b3089-4ba1-9479-73b6-84f4d49b52d8, GetStringArray method [Direct3D 10], GetStringArray method [Direct3D 10], ID3D10EffectStringVariable interface, GetStringArray,ID3D10EffectStringVariable.GetStringArray, ID3D10EffectStringVariable, ID3D10EffectStringVariable interface [Direct3D 10], GetStringArray method, ID3D10EffectStringVariable::GetStringArray, d3d10effect/ID3D10EffectStringVariable::GetStringArray, direct3d10.id3d10effectstringvariable_getstringarray
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
-	ID3D10EffectStringVariable.GetStringArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectStringVariable::GetStringArray method


## -description


Get an array of strings.


## -parameters




### -param ppStrings [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a>*</b>

A pointer to the first string in the array.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset (in number of strings) between the start of the array and the first string to get.


### -param Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of strings in the returned array.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b388e9fd-f931-46e5-a194-d832c347003a">ID3D10EffectStringVariable Interface</a>
 

 

