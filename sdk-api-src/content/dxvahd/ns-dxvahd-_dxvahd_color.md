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

# _DXVAHD_COLOR structure


## -description


Defines a color value for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field RGB

A <a href="https://msdn.microsoft.com/60a167cb-f95e-4eb5-995f-be4cceaee47d">DXVAHD_COLOR_RGBA</a> structure that contains an RGB color value.


### -field YCbCr

A <a href="https://msdn.microsoft.com/3e37daf1-5529-4042-ab6e-89a7f77d5e15">DXVAHD_COLOR_YCbCrA</a> structure that contains a YCbCr color value.


## -remarks



This union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.




## -see-also




<a href="https://msdn.microsoft.com/03d97d26-714d-4aec-bb92-0772f09b7cca">Media Foundation Unions</a>
 

 

