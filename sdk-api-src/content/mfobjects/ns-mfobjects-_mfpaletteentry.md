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

# _MFPaletteEntry structure


## -description


Contains one palette entry in a color table.


## -struct-fields




### -field ARGB


<a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that contains an RGB color.


### -field AYCbCr


<a href="https://msdn.microsoft.com/9784b561-3b87-4df9-a434-55e12f97b05a">MFAYUVSample</a> structure that contains a Y'Cb'Cr' color.


## -remarks



This union can be used to represent both RGB palettes and Y'Cb'Cr' palettes. The video format that defines the palette determines which union member should be used.




## -see-also




<a href="https://msdn.microsoft.com/03d97d26-714d-4aec-bb92-0772f09b7cca">Media Foundation Unions</a>
 

 

