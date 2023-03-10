---
UID: NF:gdiplusheaders.Region.IsVisible(constRect&,constGraphics)
title: Region::IsVisible(IN const Rect &,IN const Graphics) (gdiplusheaders.h)
description: The Region::IsVisible method determines whether a rectangle intersects this region. (overload 2/4)
helpviewer_keywords: ["IsVisible","IsVisible method [GDI+]","IsVisible method [GDI+]","Region class","Region class [GDI+]","IsVisible method","Region.IsVisible","Region.IsVisible(IN const Rect &","IN const Graphics)","Region.IsVisible(const Rect&","const Graphics*)","Region::IsVisible","Region::IsVisible(IN const Rect &","IN const Graphics)","_gdiplus_CLASS_Region_IsVisible_Rect_rect_Graphics_g_","gdiplus._gdiplus_CLASS_Region_IsVisible_Rect_rect_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_Rect_rect_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_30rectamprect_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN const Rect &,IN const Graphics), Region.IsVisible(const Rect&,const Graphics*), Region::IsVisible, Region::IsVisible(IN const Rect &,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_Rect_rect_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_Rect_rect_Graphics_g_
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

# Region::IsVisible(IN const Rect &,IN const Graphics)


## -description

The <b>Region::IsVisible</b> method determines whether a rectangle intersects this region.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle to test.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle. The default value is <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the rectangle intersects this region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>

#### Examples



The following example creates a region from a path and then tests to determine whether a rectangle intersects the region.


```cpp
VOID Example_IsVisibleRect(HDC hdc)
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

   // Check to see whether a rectangle intersects the region.
   Rect testRect(65, 25, 70, 30);

   if(pathRegion.IsVisible(testRect, &graphics))
   {
      // All or part of the rectangle is in the region.
   }

   // Draw the test rectangle.
   Pen pen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&pen, testRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>
