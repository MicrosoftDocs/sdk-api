---
UID: NS:windef.tagSIZE
title: tagSIZE
author: windows-driver-content
description: The SIZE structure specifies the width and height of a rectangle.
old-location: gdi\size.htm
old-project: gdi
ms.assetid: 8cb0802c-1868-4f3b-8287-c6fb1fa7ab68
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPSIZE, *PSIZE, *PSIZEL, PSIZE, PSIZE structure pointer [Windows GDI], SIZE, SIZE structure [Windows GDI], SIZEL, _win32_SIZE_str, gdi.size, tagSIZE, windef/PSIZE, windef/SIZE"
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
req.typenames: SIZE, *PSIZE, *LPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windef.h
api_name:
-	SIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagSIZE structure


## -description



The <b>SIZE</b> structure specifies the width and height of a rectangle.




## -struct-fields




### -field cx

Specifies the rectangle's width. The units depend on which function uses this.


### -field cy

Specifies the rectangle's height. The units depend on which function uses this.


## -remarks



The rectangle dimensions stored in this structure may correspond to viewport extents, window extents, text extents, bitmap dimensions, or the aspect-ratio filter for some extended functions.




## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/3f2dd47d-08bf-4848-897f-5ae506fba342">GetAspectRatioFilterEx</a>



<a href="https://msdn.microsoft.com/3e4f5afc-26d3-4fb2-8d00-183165fdf471">GetBitmapDimensionEx</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/e3fc188a-3796-497d-9d86-f116e9e48e30">GetViewportExtEx</a>



<a href="https://msdn.microsoft.com/17f41fcb-c9a4-4b7e-acde-73450044413e">GetWindowExtEx</a>



<a href="https://msdn.microsoft.com/8dde1322-82d7-4069-9655-a7bd3a324cb0">ScaleViewportExtEx</a>



<a href="https://msdn.microsoft.com/c34f0978-74dd-4839-99f2-a106f3d2c0f9">ScaleWindowExtEx</a>



<a href="https://msdn.microsoft.com/23960533-de71-4bff-a43f-75e5fe38fbec">SetBitmapDimensionEx</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>
 

 

