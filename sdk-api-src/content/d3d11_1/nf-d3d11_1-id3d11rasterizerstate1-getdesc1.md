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

# ID3D11RasterizerState1::GetDesc1


## -description


Gets the description for rasterizer state that you used to create the rasterizer-state object.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/7A0E526E-9352-408F-8B11-1B7A9FBC2BE1">
            D3D11_RASTERIZER_DESC1</a> structure that receives a description of the rasterizer state. This rasterizer state can specify forced sample count.


## -returns



Returns nothing.




## -remarks



You use the description for rasterizer state in a call to the <a href="https://msdn.microsoft.com/EBA793F1-35AA-4586-9D5C-803BD58B1D95">ID3D11Device1::CreateRasterizerState1</a> method to create the rasterizer-state object.




## -see-also




<a href="https://msdn.microsoft.com/771BA97B-1DC4-46DD-AAB6-DFC1100F844D">ID3D11RasterizerState1</a>
 

 

