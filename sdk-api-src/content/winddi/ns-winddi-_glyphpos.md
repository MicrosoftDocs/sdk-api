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

# _GLYPHPOS structure


## -description


The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.


## -struct-fields




### -field hg

Handle to the glyph.


### -field pgdf

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a> union.


### -field ptl

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that contains the coordinates of the point in device space where the character origin of the glyph should be placed.


## -remarks








## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566822">GLYPHDEF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569739">STROBJ_bEnum</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569745">STROBJ_vEnumStart</a>
 

 

