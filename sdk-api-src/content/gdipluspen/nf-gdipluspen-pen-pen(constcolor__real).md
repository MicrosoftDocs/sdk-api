---
UID: NF:gdipluspen.Pen.Pen(constColor&,REAL)
title: Pen::Pen(IN const Color &,IN REAL) (gdipluspen.h)
description: Creates a Pen object that uses a specified color and width.
helpviewer_keywords: ["Pen","Pen class [GDI+]","Pen constructor","Pen constructor [GDI+]","Pen constructor [GDI+]","Pen class","Pen.Pen","Pen.Pen(IN const Color &","IN REAL)","Pen.Pen(const Color&","REAL)","Pen::Pen","Pen::Pen(IN const Color &","IN REAL)","_gdiplus_CLASS_Pen_Pen_color_width_","gdiplus._gdiplus_CLASS_Pen_Pen_color_width_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_Pen_color_width_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penconstructors\pen_36color_width.htm
ms.date: 12/05/2018
ms.keywords: Pen, Pen class [GDI+],Pen constructor, Pen constructor [GDI+], Pen constructor [GDI+],Pen class, Pen.Pen, Pen.Pen(IN const Color &,IN REAL), Pen.Pen(const Color&,REAL), Pen::Pen, Pen::Pen(IN const Color &,IN REAL), _gdiplus_CLASS_Pen_Pen_color_width_, gdiplus._gdiplus_CLASS_Pen_Pen_color_width_
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Pen::Pen
 - gdipluspen/Pen::Pen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.Pen
---

# Pen::Pen(IN const Color &,IN REAL)


## -description

Creates a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object that uses a specified color and width.

## -parameters

### -param color [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color for this <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

### -param width [in]

Type: <b>REAL</b>

Optional. Real number that specifies the width of this pen's stroke. The default value is 1.0.  If this value is 0, the width in device units is always 1 pixel, except that the `width` will not be affected by scale-transform operations that are in effect for the Graphics object that the <xref:System.Drawing.Pen> is used for; the width will always be 1 pixel.

## -remarks

If you pass the address of a pen to one of the draw methods of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is <b>UnitPixel</b>, which is an element of the 
				<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object with the color red and a width of 4.0.


```cpp
Pen pen(Color(255,255,0,0), 4.0f); 
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setwidth">Pen::SetWidth</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>
