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

# MAKEROP4 macro


## -description



The <b>MAKEROP4</b> macro creates a quaternary raster operation code for use with the <a href="https://msdn.microsoft.com/9fd6f0ce-a802-428d-9be5-a66afe39e9b7">MaskBlt</a> function. The macro takes two ternary raster operation codes as input, one for the foreground and one for the background, and packs their Boolean operation indexes into the high-order word of a 32-bit value. The low-order word of this value will be ignored.




## -parameters




### -param fore

The foreground ternary raster operation code.


### -param back

The background ternary raster operation code.


## -see-also




<a href="https://msdn.microsoft.com/8781bbf4-89fe-4212-b9df-e5b5cb07528c">Bitmap Macros</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9fd6f0ce-a802-428d-9be5-a66afe39e9b7">MaskBlt</a>
 

 

