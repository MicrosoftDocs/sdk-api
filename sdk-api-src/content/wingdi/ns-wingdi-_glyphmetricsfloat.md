---
UID: NS:wingdi._GLYPHMETRICSFLOAT
title: "_GLYPHMETRICSFLOAT"
author: windows-sdk-content
description: The GLYPHMETRICSFLOAT structure contains information about the placement and orientation of a glyph in a character cell.
old-location: opengl\glyphmetricsfloat.htm
tech.root: OpenGL
ms.assetid: 6ceccb76-be31-4a4d-b093-1f8e35261a60
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPGLYPHMETRICSFLOAT, *PGLYPHMETRICSFLOAT, GLYPHMETRICSFLOAT, GLYPHMETRICSFLOAT structure [OpenGL], PGLYPHMETRICSFLOAT, PGLYPHMETRICSFLOAT structure pointer [OpenGL], _GLYPHMETRICSFLOAT, _ogl_GLYPHMETRICSFLOAT, opengl.glyphmetricsfloat, wingdi/GLYPHMETRICSFLOAT, wingdi/PGLYPHMETRICSFLOAT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - GLYPHMETRICSFLOAT
product: Windows
targetos: Windows
req.typenames: GLYPHMETRICSFLOAT, *PGLYPHMETRICSFLOAT, *LPGLYPHMETRICSFLOAT
req.redist: 
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



<a href="https://msdn.microsoft.com/109c41b1-d3d2-4c1d-9809-99a0a89df263">Structures</a>



<a href="https://msdn.microsoft.com/08a86563-c6ca-4efb-9096-bc487fc5037c">wglUseFontOutlines</a>
 

 

