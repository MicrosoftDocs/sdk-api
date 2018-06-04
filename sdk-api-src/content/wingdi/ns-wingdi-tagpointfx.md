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

# tagPOINTFX structure


## -description



The <b>POINTFX</b> structure contains the coordinates of points that describe the outline of a character in a TrueType font.




## -struct-fields




### -field x

The x-component of a point on the outline of a TrueType character.


### -field y

The y-component of a point on the outline of a TrueType character.


## -remarks



The <b>POINTFX</b> structure is a member of the <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> and <a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a> structures. Values in the <b>POINTFX</b> structure are specified in device units.




## -see-also




<a href="https://msdn.microsoft.com/b1d94060-e822-447f-82ba-fd1cf2ddaa3b">FIXED</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a>



<a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a>
 

 

