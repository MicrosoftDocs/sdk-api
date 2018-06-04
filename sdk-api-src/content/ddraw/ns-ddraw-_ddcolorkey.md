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

# _DDCOLORKEY structure


## -description


The <b>DDCOLORKEY</b> structure describes a source color key, destination color key, or color space. A color key is specified if the low and high range values are the same. This structure is used with the <a href="https://msdn.microsoft.com/0df14c63-f962-4823-873a-3fe1d626f4cb">IDirectDrawSurface7::GetColorKey</a> and <a href="https://msdn.microsoft.com/36f2510e-d12a-40af-b65c-aa36ce46a942">IDirectDrawSurface7::SetColorKey</a> methods.




## -struct-fields




### -field dwColorSpaceLowValue

Low value of the color range that is to be used as the color key.


### -field dwColorSpaceHighValue

High value of the color range that is to be used as the color key.

