---
UID: NF:d3d10effect.ID3D10EffectVariable.GetRawValue
title: ID3D10EffectVariable::GetRawValue (d3d10effect.h)
author: windows-sdk-content
description: Get data.
old-location: direct3d10\id3d10effectvariable_getrawvalue.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getrawvalue.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 18ba7994-4337-bf43-0492-e591b629b77d, GetRawValue, GetRawValue method [Direct3D 10], GetRawValue method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetRawValue method, ID3D10EffectVariable.GetRawValue, ID3D10EffectVariable::GetRawValue, d3d10effect/ID3D10EffectVariable::GetRawValue, direct3d10.id3d10effectvariable_getrawvalue
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
 - ID3D10EffectVariable.GetRawValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10EffectVariable::GetRawValue


## -description


Get data.


## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to the variable.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset (in bytes) from the beginning of the pointer to the data.


### -param ByteCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes to get.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method does no conversion or type checking; it is therefore a very quick way to access array items.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

