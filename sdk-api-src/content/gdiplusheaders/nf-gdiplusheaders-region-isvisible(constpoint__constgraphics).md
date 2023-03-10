---
UID: NF:gdiplusheaders.Region.IsVisible(constPoint&,constGraphics)
title: Region::IsVisible(IN const Point &,IN const Graphics) (gdiplusheaders.h)
description: The Region::IsVisible method determines whether a point is inside this region. (overload 1/4)
helpviewer_keywords: ["IsVisible","IsVisible method [GDI+]","IsVisible method [GDI+]","Region class","Region class [GDI+]","IsVisible method","Region.IsVisible","Region.IsVisible(IN const Point &","IN const Graphics)","Region.IsVisible(const Point&","const Graphics*)","Region::IsVisible","Region::IsVisible(IN const Point &","IN const Graphics)","_gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_","gdiplus._gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_84pointamppoint_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN const Point &,IN const Graphics), Region.IsVisible(const Point&,const Graphics*), Region::IsVisible, Region::IsVisible(IN const Point &,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_
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

# Region::IsVisible(IN const Point &,IN const Graphics)


## -description

The <b>Region::IsVisible</b> method determines whether a point is inside this region.

## -parameters

### -param point [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point to test.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the point. The default value is <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the point is inside this region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>

#### Examples



The following example creates a region from a path and then tests to determine whether a point is in the region.


```cpp
VOID Example_IsVisiblePoint(HDC hdc)
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

   // Check to see whether a point is in the region.
   Point testPoint(125, 30);

   if(pathRegion.IsVisible(testPoint, &graphics))
   {
      // The test point is in the region.
   }

   // Fill a small circle centered at the test point.
   SolidBrush brush(Color(255, 0, 0, 0));
   graphics.FillEllipse(&brush, testPoint.X - 4, testPoint.Y - 4, 8, 8);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
