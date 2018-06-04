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

# tagTTPOLYGONHEADER structure


## -description



The <b>TTPOLYGONHEADER</b> structure specifies the starting position and type of a contour in a TrueType character outline.




## -struct-fields




### -field cb

The number of bytes required by the <b>TTPOLYGONHEADER</b> structure and <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> structure or structures required to describe the contour of the character.


### -field dwType

The type of character outline returned. Currently, this value must be TT_POLYGON_TYPE.


### -field pfxStart

The starting point of the contour in the character outline.


## -remarks



Each <b>TTPOLYGONHEADER</b> structure is followed by one or more <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a>



<a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a>
 

 

