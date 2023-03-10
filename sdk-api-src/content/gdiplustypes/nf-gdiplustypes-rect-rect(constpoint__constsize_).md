---
UID: NF:gdiplustypes.Rect.Rect(constPoint&,constSize&)
title: Rect::Rect(IN const Point &,IN const Size &) (gdiplustypes.h)
description: Creates a Rect object by using a Point object to initialize the X and Y data members and a Size object to initialize the Width and Height data members.
helpviewer_keywords: ["Rect","Rect class [GDI+]","Rect constructor","Rect constructor [GDI+]","Rect constructor [GDI+]","Rect class","Rect.Rect","Rect.Rect(IN const Point &","IN const Size &)","Rect.Rect(const Point&","const Size&)","Rect::Rect","Rect::Rect(IN const Point &","IN const Size &)","_gdiplus_CLASS_Rect_Rect_location_size_","gdiplus._gdiplus_CLASS_Rect_Rect_location_size_"]
old-location: gdiplus\_gdiplus_CLASS_Rect_Rect_location_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectconstructors\rect_65location_size.htm
ms.date: 12/05/2018
ms.keywords: Rect, Rect class [GDI+],Rect constructor, Rect constructor [GDI+], Rect constructor [GDI+],Rect class, Rect.Rect, Rect.Rect(IN const Point &,IN const Size &), Rect.Rect(const Point&,const Size&), Rect::Rect, Rect::Rect(IN const Point &,IN const Size &), _gdiplus_CLASS_Rect_Rect_location_size_, gdiplus._gdiplus_CLASS_Rect_Rect_location_size_
req.header: gdiplustypes.h
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
 - Rect::Rect
 - gdiplustypes/Rect::Rect
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
 - Rect.Rect
---

# Rect::Rect(IN const Point &,IN const Size &)


## -description

Creates a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object by using a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object to initialize the 
			<b>Width</b> and 
			<b>Height</b> data members.

## -parameters

### -param location [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that specifies the upper-left corner of this rectangle.

### -param size [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object that specifies the width and height of this rectangle.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-class-rect-constructors">Rect Constructors</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>