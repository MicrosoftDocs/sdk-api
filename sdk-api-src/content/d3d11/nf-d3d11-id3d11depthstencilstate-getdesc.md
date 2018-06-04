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

# ID3D11DepthStencilState::GetDesc


## -description


Gets the description for depth-stencil state that you used to create the depth-stencil-state object.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a> structure that receives a description of the depth-stencil state.


## -returns



Returns nothing.




## -remarks



You use the description for depth-stencil state in a call to the <a href="https://msdn.microsoft.com/7577604c-922c-408c-8eab-2361ebda17df">ID3D11Device::CreateDepthStencilState</a> method to create the depth-stencil-state object.




## -see-also




<a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>
 

 

