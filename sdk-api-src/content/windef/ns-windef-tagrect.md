---
UID: NS:windef.tagRECT
title: tagRECT
author: windows-driver-content
description: The RECT structure defines the coordinates of the upper-left and lower-right corners of a rectangle.
old-location: gdi\rect.htm
old-project: gdi
ms.assetid: 9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPRECT, *NPRECT, *PRECT, PRECT, PRECT structure pointer [Windows GDI], RECT, RECT structure [Windows GDI], _win32_RECT_str, gdi.rect, tagRECT, windef/PRECT, windef/RECT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windef.h
req.include-header: Windows.h
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
req.typenames: RECT, *PRECT, *NPRECT, *LPRECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windef.h
api_name:
-	RECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagRECT structure


## -description



The <b>RECT</b> structure defines the coordinates of the upper-left and lower-right corners of a rectangle.




## -struct-fields




### -field left

The x-coordinate of the upper-left corner of the rectangle.


### -field top

The y-coordinate of the upper-left corner of the rectangle.


### -field right

The x-coordinate of the lower-right corner of the rectangle.


### -field bottom

The y-coordinate of the lower-right corner of the rectangle.


## -remarks



By convention, the right and bottom edges of the rectangle are normally considered exclusive. In other words, the pixel whose coordinates are ( <b>right</b>, <b>bottom</b> ) lies immediately outside of the rectangle. For example, when <b>RECT</b> is passed to the <a href="https://msdn.microsoft.com/98ab34da-ea07-4446-a62e-509c849d95f9">FillRect</a> function, the rectangle is filled up to, but not including, the right column and bottom row of pixels. This structure is identical to the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/98ab34da-ea07-4446-a62e-509c849d95f9">FillRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>



<a href="https://msdn.microsoft.com/88700dde-2559-4916-9445-0fdd73da7501">Rectangle Structures</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>
 

 

