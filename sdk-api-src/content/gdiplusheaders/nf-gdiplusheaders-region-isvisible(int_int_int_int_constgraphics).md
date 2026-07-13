---
UID: NF:gdiplusheaders.Region.IsVisible(INT,INT,INT,INT,constGraphics)
title: Region::IsVisible(IN INT,IN INT,IN INT,IN INT,IN const Graphics) (gdiplusheaders.h)
description: The Region::IsVisible method determines whether a rectangle intersects this region. (overload 3/4)
helpviewer_keywords: ["IsVisible","IsVisible method [GDI+]","IsVisible method [GDI+]","Region class","Region class [GDI+]","IsVisible method","Region.IsVisible","Region.IsVisible(IN INT","IN INT","IN INT","IN INT","IN const Graphics)","Region.IsVisible(INT","INT","INT","INT","const Graphics*)","Region::IsVisible","Region::IsVisible(IN INT","IN INT","IN INT","IN INT","IN const Graphics)","_gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_INT_width_INT_height_Graphics_g_","gdiplus._gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_INT_width_INT_height_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_INT_width_INT_height_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_53intx_inty_intwidth_intheight_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN INT,IN INT,IN INT,IN INT,IN const Graphics), Region.IsVisible(INT,INT,INT,INT,const Graphics*), Region::IsVisible, Region::IsVisible(IN INT,IN INT,IN INT,IN INT,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_INT_width_INT_height_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_INT_width_INT_height_Graphics_g_
req.header: gdiplusheaders.h
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
 - Region::IsVisible
 - gdiplusheaders/Region::IsVisible
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
 - Region.IsVisible
---

# Region::IsVisible(IN INT,IN INT,IN INT,IN INT,IN const Graphics)


## -description

The <b>Region::IsVisible</b> method determines whether a rectangle intersects this region.

## -parameters

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle to test.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle to test.

### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle to test.

### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle to test.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle. The default value is <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the rectangle intersects this region, the method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>

#### Examples



The following example creates a region from a path and then tests to determine whether a rectangle intersects the region.


```cpp
VOID Example_IsVisibleXYWH(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   GraphicsPath path;
   SolidBrush solidBrush(Color(255, 255, 0, 0));

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&path);
   graphics.FillRegion(&solidBrush, &pathRegion);

   // Check to see whether the rectangle intersects the region.
   // The rectangle has upper-left corner (65, 25), width 70, and height 30.
   if(pathRegion.IsVisible(65, 25, 70, 30, &graphics))
   {
      // All or part of the rectangle is in the region.
   }

   // Draw the rectangle.
   Pen pen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&pen, 65, 25, 70, 30);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>
