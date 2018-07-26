---
UID: NF:d3d10effect.ID3D10EffectVariable.SetRawValue
title: ID3D10EffectVariable::SetRawValue
author: windows-sdk-content
description: Set data.
old-location: direct3d10\id3d10effectvariable_setrawvalue.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_setrawvalue.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 43b4261f-2644-4897-99db-041ae06099f3, ID3D10EffectVariable interface [Direct3D 10],SetRawValue method, ID3D10EffectVariable.SetRawValue, ID3D10EffectVariable::SetRawValue, SetRawValue, SetRawValue method [Direct3D 10], SetRawValue method [Direct3D 10],ID3D10EffectVariable interface, d3d10effect/ID3D10EffectVariable::SetRawValue, direct3d10.id3d10effectvariable_setrawvalue
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
 - ID3D10EffectVariable.SetRawValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectVariable::SetRawValue


## -description


Set data.


## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to the variable.


### -param Offset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset (in bytes) from the beginning of the pointer to the data.


### -param ByteCount






#### - Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes to set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method does no conversion or type checking; it is therefore a very quick way to access array items.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173724(v=VS.85).aspx">ID3D10EffectVariable Interface</a>
 

 

