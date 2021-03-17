---
UID: NF:gdiplustypes.Rect.Equals
title: Rect::Equals (gdiplustypes.h)
description: The Rect::Equals method determines whether two rectangles are the same.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","Rect class","Rect class [GDI+]","Equals method","Rect.Equals","Rect::Equals","_gdiplus_CLASS_Rect_Equals_rect_","gdiplus._gdiplus_CLASS_Rect_Equals_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Rect_Equals_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\equals_42rect.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Rect class, Rect class [GDI+],Equals method, Rect.Equals, Rect::Equals, _gdiplus_CLASS_Rect_Equals_rect_, gdiplus._gdiplus_CLASS_Rect_Equals_rect_
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
 - Rect::Equals
 - gdiplustypes/Rect::Equals
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
 - Rect.Equals
---

# Rect::Equals


## -description

The <b>Rect::Equals</b> method determines whether two rectangles are the same.

## -parameters

### -param rect [in]

Type: <b>const Rect&amp;</b>

Reference to a rectangle to compare to this rectangle.

## -returns

Type: <b>BOOL</b>

If the rectangles are the same, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

Two rectangles are the same if their 
				<b>X</b>, 
				<b>Y</b>, 
				<b>Width</b>, and 
				<b>Height</b> data members are the same.


#### Examples



The following example creates two 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> objects, moves the second 
						<b>Rect</b> object horizontally by a specified value, and then determines whether the two 
						<b>Rect</b> objects are the same.


```cpp
Rect rect1(50, 50, 200, 100);
Rect rect2(20, 50, 200, 100);

rect2.Offset(30, 0);

if(rect2.Equals(rect1))
{
   // The two rectangles are the same.
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>