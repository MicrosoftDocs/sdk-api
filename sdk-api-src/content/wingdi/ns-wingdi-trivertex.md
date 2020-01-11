---
UID: NS:wingdi._TRIVERTEX
title: TRIVERTEX (wingdi.h)
description: The TRIVERTEX structure contains color information and position information.
old-location: gdi\trivertex.htm
tech.root: gdi
ms.assetid: 47b700aa-3410-4610-ba06-dab2b2662f5e
ms.date: 12/05/2018
ms.keywords: '*LPTRIVERTEX, *PTRIVERTEX, PTRIVERTEX, PTRIVERTEX structure pointer [Windows GDI], TRIVERTEX, TRIVERTEX structure [Windows GDI], _win32_TRIVERTEX_str, gdi.trivertex, wingdi/PTRIVERTEX, wingdi/TRIVERTEX'
f1_keywords:
- wingdi/TRIVERTEX
dev_langs:
- c++
req.header: wingdi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wingdi.h
api_name:
- TRIVERTEX
targetos: Windows
req.typenames: TRIVERTEX, *PTRIVERTEX, *LPTRIVERTEX
req.redist: 
ms.custom: 19H1
---

# TRIVERTEX structure


## -description



The <b>TRIVERTEX</b> structure contains color information and position information.




## -struct-fields




### -field x

The x-coordinate, in logical units, of the upper-left corner of the rectangle.


### -field y

The y-coordinate, in logical units, of the upper-left corner of the rectangle.


### -field Red

The color information at the point of x, y.


### -field Green

The color information at the point of x, y.


### -field Blue

The color information at the point of x, y.


### -field Alpha

The color information at the point of x, y.


## -remarks



In the <b>TRIVERTEX</b> structure, x and y indicate position in the same manner as in the <a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a> structure contained in the wtypes.h header file. <b>Red</b>, <b>Green</b>, <b>Blue</b>, and <b>Alpha</b> members indicate color information at the point x, y. The color information of each channel is specified as a value from 0x0000 to 0xff00. This allows higher color resolution for an object that has been split into small triangles for display. The <b>TRIVERTEX</b> structure contains information needed by the <i>pVertex</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>.


#### Examples

For an example of the use of this structure, see <a href="https://docs.microsoft.com/windows/desktop/gdi/drawing-a-shaded-triangle">Drawing a Shaded Triangle</a> or <a href="https://docs.microsoft.com/windows/desktop/gdi/drawing-a-shaded-rectangle">Drawing a Shaded Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>



<a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a>
 

 

