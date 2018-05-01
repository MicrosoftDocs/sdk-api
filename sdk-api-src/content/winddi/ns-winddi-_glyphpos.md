---
UID: NS:winddi._GLYPHPOS
title: "_GLYPHPOS"
author: windows-driver-content
description: The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.
old-location: display\glyphpos.htm
old-project: display
ms.assetid: 1eb80e7a-93f5-474c-bed9-5b19f6657788
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PGLYPHPOS, GLYPHPOS, GLYPHPOS structure [Display Devices], PGLYPHPOS, PGLYPHPOS structure pointer [Display Devices], _GLYPHPOS, display.glyphpos, grstrcts_52c5687f-a40b-43c6-8513-accd4c72def5.xml, winddi/GLYPHPOS, winddi/PGLYPHPOS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: GLYPHPOS, *PGLYPHPOS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	GLYPHPOS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

