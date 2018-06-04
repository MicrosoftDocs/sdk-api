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

# ID3D11BlendState1::GetDesc1


## -description


Gets the description for blending state that you used to create the blend-state object.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/BBBECB86-B33D-4AA3-8D0A-45AEC3BBC4AB">D3D11_BLEND_DESC1</a> structure that receives a description of the blend state. This blend state can specify logical operations as well as blending operations.


## -returns



Returns nothing.




## -remarks



You use the description for blending state in a call to the <a href="https://msdn.microsoft.com/2E891104-3706-46A5-88FB-C621C95B4EFB">ID3D11Device1::CreateBlendState1</a> method to create the blend-state object.




## -see-also




<a href="https://msdn.microsoft.com/5562F0B2-77FC-4614-BFA9-077323D4A2FA">ID3D11BlendState1</a>
 

 

