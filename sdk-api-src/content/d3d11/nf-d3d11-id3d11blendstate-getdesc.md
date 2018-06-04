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

# ID3D11BlendState::GetDesc


## -description


Gets the description for blending state that you used to create the blend-state object.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a> structure that receives a description of the blend state.


## -returns



Returns nothing.




## -remarks



You use the description for blending state in a call to the <a href="https://msdn.microsoft.com/05b27d72-6ae5-4bab-8906-2d1373ea8d4c">ID3D11Device::CreateBlendState</a> method to create the blend-state object.




## -see-also




<a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>
 

 

