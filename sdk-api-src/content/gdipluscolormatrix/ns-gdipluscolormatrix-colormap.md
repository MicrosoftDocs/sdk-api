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

# ColorMap structure


## -description


The <b>ColorMap</b> structure contains two <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects. Several methods of the <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> class adjust image colors by using a color remap table, which is an array of <b>ColorMap</b> structures.


## -struct-fields




### -field oldColor

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

The original color. 


### -field newColor

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

The new color. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122">Using a Color Remap Table</a>
 

 

