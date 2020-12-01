---
UID: NF:gdiplusbrush.LinearGradientBrush.GetRectangle(Rect)
title: LinearGradientBrush::GetRectangle(OUT Rect) (gdiplusbrush.h)
description: The LinearGradientBrush::GetRectangle method gets the rectangle that defines the boundaries of the gradient.
helpviewer_keywords: ["GetRectangle","GetRectangle method [GDI+]","GetRectangle method [GDI+]","LinearGradientBrush class","LinearGradientBrush class [GDI+]","GetRectangle method","LinearGradientBrush.GetRectangle","LinearGradientBrush.GetRectangle(OUT Rect)","LinearGradientBrush.GetRectangle(Rect*)","LinearGradientBrush::GetRectangle","LinearGradientBrush::GetRectangle(OUT Rect)","_gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_","gdiplus._gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\lineargradientbrushgetrectanglemethods\getrectangle.htm
ms.date: 12/05/2018
ms.keywords: GetRectangle, GetRectangle method [GDI+], GetRectangle method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetRectangle method, LinearGradientBrush.GetRectangle, LinearGradientBrush.GetRectangle(OUT Rect), LinearGradientBrush.GetRectangle(Rect*), LinearGradientBrush::GetRectangle, LinearGradientBrush::GetRectangle(OUT Rect), _gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_
req.header: gdiplusbrush.h
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
 - LinearGradientBrush::GetRectangle
 - gdiplusbrush/LinearGradientBrush::GetRectangle
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
 - LinearGradientBrush.GetRectangle
---

# LinearGradientBrush::GetRectangle(OUT Rect)


## -description

The <b>LinearGradientBrush::GetRectangle</b> method gets the rectangle that defines the boundaries of the gradient.

## -parameters

### -param rect [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the rectangle that defines the boundaries of the gradient. For example, if a linear gradient brush is constructed with a starting point at (20, 50) and an ending point at (60, 110), then the defining rectangle has its upper-left point at (20, 50), a width of 40, and a height of 60.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The rectangle defines the boundaries of the gradient in the following ways: The right and left sides of the rectangle form the boundaries of a horizontal gradient. The top and bottom sides form the boundaries of a vertical gradient. Two of the diagonally opposing corners lie on the boundaries of a diagonal gradient. In each of these cases, either side/corner may be on the starting boundary, depending on how the starting and ending points are passed to the constructor.


#### Examples



The following example creates a linear gradient brush. Then the code gets the brush's rectangle and draws it.


```cpp
VOID Example_GetRect(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Create a linear gradient brush.
   LinearGradientBrush linGrBrush( 
      Point(20, 10),
      Point(60, 110),
      Color(255, 0, 0, 0),     // black
      Color(255, 0, 0, 255));  // blue

   // Obtain information about the linear gradient brush.
   Rect rect;
   linGrBrush.GetRectangle(&rect);

   // Draw the retrieved rectangle.
   Pen myPen(Color(255, 0, 0, 0));
   myGraphics.DrawRectangle(&myPen, rect);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>