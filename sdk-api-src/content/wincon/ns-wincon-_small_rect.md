---
UID: NS:wincon._SMALL_RECT
title: "_SMALL_RECT"
author: windows-driver-content
description: Defines the coordinates of the upper left and lower right corners of a rectangle.
old-location: consoles\small_rect_str.htm
old-project: consoles
ms.assetid: 62639815-c7e9-4ae2-b152-61290f78422b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PSMALL_RECT, SMALL_RECT, SMALL_RECT structure [Consoles], _SMALL_RECT, _win32_small_rect_str, base.small_rect_str, consoles.small_rect_str, wincon/SMALL_RECT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
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
req.typenames: SMALL_RECT, *PSMALL_RECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	SMALL_RECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _SMALL_RECT structure


## -description


Defines the coordinates of the upper left and lower right corners of a rectangle.


## -struct-fields




### -field Left

The x-coordinate of the upper left corner of the rectangle.


### -field Top

The y-coordinate of the upper left corner of the rectangle.


### -field Right

The x-coordinate of the lower right corner of the rectangle.


### -field Bottom

The y-coordinate of the lower right corner of the rectangle.


## -remarks



This structure is used by console functions to specify rectangular areas of console screen buffers, where the coordinates specify the rows and columns of screen-buffer character cells.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/288c6a0f-fbaa-4eee-895e-a25884b7b70a">Scrolling a Screen Buffer's Contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>
 

 

