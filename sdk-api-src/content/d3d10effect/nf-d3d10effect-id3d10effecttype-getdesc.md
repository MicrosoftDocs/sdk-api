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

# ID3D10EffectType::GetDesc


## -description


Get an effect-type description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/6ed4c32f-26f7-47c0-b8dc-6520364113e9">D3D10_EFFECT_TYPE_DESC</a>*</b>

A pointer to an effect-type description. See <a href="https://msdn.microsoft.com/6ed4c32f-26f7-47c0-b8dc-6520364113e9">D3D10_EFFECT_TYPE_DESC</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.




## -see-also




<a href="https://msdn.microsoft.com/8b396c86-82de-4a0e-8b86-228e3716c09b">ID3D10EffectType Interface</a>
 

 

