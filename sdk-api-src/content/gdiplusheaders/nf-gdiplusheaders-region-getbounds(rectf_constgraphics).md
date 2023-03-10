---
UID: NF:gdiplusheaders.Region.GetBounds(RectF,constGraphics)
title: Region::GetBounds(OUT RectF,IN const Graphics) (gdiplusheaders.h)
description: The Region::GetBounds method gets a rectangle that encloses this region. (overload 1/2)
helpviewer_keywords: ["GetBounds","GetBounds method [GDI+]","GetBounds method [GDI+]","Region class","Region class [GDI+]","GetBounds method","Region.GetBounds","Region.GetBounds(OUT RectF","IN const Graphics)","Region.GetBounds(RectF*","const Graphics*)","Region::GetBounds","Region::GetBounds(OUT RectF","IN const Graphics)","_gdiplus_CLASS_Region_GetBounds_RectF_rect_Graphics_g_","gdiplus._gdiplus_CLASS_Region_GetBounds_RectF_rect_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_GetBounds_RectF_rect_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiongetboundsmethods\getbounds_96rectfrect_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],Region class, Region class [GDI+],GetBounds method, Region.GetBounds, Region.GetBounds(OUT RectF,IN const Graphics), Region.GetBounds(RectF*,const Graphics*), Region::GetBounds, Region::GetBounds(OUT RectF,IN const Graphics), _gdiplus_CLASS_Region_GetBounds_RectF_rect_Graphics_g_, gdiplus._gdiplus_CLASS_Region_GetBounds_RectF_rect_Graphics_g_
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
 - Region::GetBounds
 - gdiplusheaders/Region::GetBounds
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
 - Region.GetBounds
---

# Region::GetBounds(OUT RectF,IN const Graphics)


## -description

The <b>Region::GetBounds</b> method gets a rectangle that encloses this region.

## -parameters

### -param rect [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the enclosing rectangle.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The current world and page transformations of the graphics object are used to calculate the region and the rectangle as they are drawn on the display device. The rectangle returned by <b>Region::GetBounds</b> is not always the smallest possible rectangle.


#### Examples



The following example creates a region from a path, gets the region's enclosing rectangle, and then displays both.


```cpp
VOID Example_GetBoundsRectF(HDC hdc)
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
    Pen pen(Color(255, 0, 0, 0));
    RectF rect;

   path.AddClosedCurve(points, 6);

    // Create a region from a path.
    Region pathRegion(&path);
    
    // Get the region's enclosing rectangle.
    pathRegion.GetBounds(&rect, &graphics);

    // Show the region and the enclosing rectangle.
    graphics.FillRegion(&solidBrush, &pathRegion);
    graphics.DrawRectangle(&pen, rect);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>
