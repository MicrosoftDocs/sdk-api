---
UID: NF:d3d10effect.ID3D10EffectVariable.GetRawValue
title: ID3D10EffectVariable::GetRawValue
author: windows-sdk-content
description: Get data.
old-location: direct3d10\id3d10effectvariable_getrawvalue.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectvariable_getrawvalue.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 18ba7994-4337-bf43-0492-e591b629b77d, GetRawValue, GetRawValue method [Direct3D 10], GetRawValue method [Direct3D 10],ID3D10EffectVariable interface, ID3D10EffectVariable interface [Direct3D 10],GetRawValue method, ID3D10EffectVariable.GetRawValue, ID3D10EffectVariable::GetRawValue, d3d10effect/ID3D10EffectVariable::GetRawValue, direct3d10.id3d10effectvariable_getrawvalue
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
 - ID3D10EffectVariable.GetRawValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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


### -param ByteCount






#### - Count [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes to get.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method does no conversion or type checking; it is therefore a very quick way to access array items.




## -see-also




<a href="https://msdn.microsoft.com/55bfed47-6f5a-4eed-8389-b291e00c6f69">ID3D10EffectVariable Interface</a>
 

 

