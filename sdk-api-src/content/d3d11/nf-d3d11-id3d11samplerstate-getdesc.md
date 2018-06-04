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

# ID3D11SamplerState::GetDesc


## -description


Gets the description for sampler state that you used to create the sampler-state object.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/97dd6cac-6657-4a1e-b631-4e5d36994b16">D3D11_SAMPLER_DESC</a> structure that receives a description of the sampler state.


## -returns



Returns nothing.




## -remarks



You use the description for sampler state in a call to the <a href="https://msdn.microsoft.com/66cf7189-2882-43a4-8732-657402c983db">ID3D11Device::CreateSamplerState</a> method to create the sampler-state object.




## -see-also




<a href="https://msdn.microsoft.com/8dc2facc-4f51-4064-aab4-028a06b9d7e6">ID3D11SamplerState</a>
 

 

