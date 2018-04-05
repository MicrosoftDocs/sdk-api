---
UID: NS:windef._RECTL
title: "_RECTL"
author: windows-driver-content
description: The RECTL structure defines the coordinates of the upper-left and lower-right corners of a rectangle.
old-location: gdi\rectl.htm
old-project: gdi
ms.assetid: 47a89d2d-4733-47be-91c1-450845e78075
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPRECTL, *PRECTL, PRECTL, PRECTL structure pointer [Windows GDI], RECTL, RECTL structure [Windows GDI], _RECTL, _win32_RECTL_str, gdi.rectl, windef/PRECTL, windef/RECTL"
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
req.typenames: RECTL, *PRECTL, *LPRECTL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windef.h
api_name:
-	RECTL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _RECTL structure


## -description



The <b>RECTL</b> structure defines the coordinates of the upper-left and lower-right corners of a rectangle.




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



The <b>RECTL</b> structure is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/98ab34da-ea07-4446-a62e-509c849d95f9">FillRect</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>
 

 

