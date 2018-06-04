---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D10EffectBlendVariable::GetBackingStore


## -description


Get a pointer to a blend-state variable.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into an array of blend-state descriptions. If there is only one blend-state variable in the effect, use 0.


### -param pBlendDesc [in]

Type: <b><a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">D3D10_BLEND_DESC</a>*</b>

A pointer to a blend-state description (see <a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">D3D10_BLEND_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device. Backing store data can used to recreate the variable when necessary.




## -see-also




<a href="https://msdn.microsoft.com/0a41f4a6-e58f-4cdb-a043-eb2b4cfd2dab">ID3D10EffectBlendVariable Interface</a>
 

 

