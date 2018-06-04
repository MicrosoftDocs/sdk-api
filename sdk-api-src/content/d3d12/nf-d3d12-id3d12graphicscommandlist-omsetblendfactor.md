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

# ID3D12GraphicsCommandList::OMSetBlendFactor


## -description


Sets the blend factor that modulate values for a pixel shader, render target, or both.


## -parameters




### -param BlendFactor [in, optional]

Type: <b>const FLOAT[4]</b>


            Array of blend factors, one for each RGBA component.
          


## -returns




            This method does not return a value.
          




## -remarks




        If you created the blend-state object with D3D11_BLEND_BLEND_FACTOR or D3D11_BLEND_INV_BLEND_FACTOR, the blending stage uses the non-NULL array of blend factors.
      


        If you didn't create the blend-state object with D3D11_BLEND_BLEND_FACTOR or D3D11_BLEND_INV_BLEND_FACTOR, the blending stage does not use the non-NULL array of blend factors; the runtime stores the blend factors.
      


        If you pass NULL, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.
      


        D3D11_BLEND_BLEND_FACTOR and D3D11_BLEND_INV_BLEND_FACTOR are <a href="https://msdn.microsoft.com/BA114E1C-0E0B-4260-ACED-0FF3D426C764">D3D12_BLEND</a> enumeration constants.
      




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

