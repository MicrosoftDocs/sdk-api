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

# _GLYPHMETRICSFLOAT structure


## -description



The <b>GLYPHMETRICSFLOAT</b> structure contains information about the placement and orientation of a glyph in a character cell.




## -struct-fields




### -field gmfBlackBoxX

Specifies the width of the smallest rectangle (the glyph's black box) that completely encloses the glyph.


### -field gmfBlackBoxY

Specifies the height of the smallest rectangle (the glyph's black box) that completely encloses the glyph.


### -field gmfptGlyphOrigin

Specifies the x and y coordinates of the upper-left corner of the smallest rectangle that completely encloses the glyph.


### -field gmfCellIncX

Specifies the horizontal distance from the origin of the current character cell to the origin of the next character cell.


### -field gmfCellIncY

Specifies the vertical distance from the origin of the current character cell to the origin of the next character cell.


## -remarks



The values of <b>GLYPHMETRICSFLOAT</b> are specified as notional units.




## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/9cb57d32-386a-4554-9f47-62d5c4e2ee4e">POINTFLOAT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/08a86563-c6ca-4efb-9096-bc487fc5037c">wglUseFontOutlines</a>
 

 

