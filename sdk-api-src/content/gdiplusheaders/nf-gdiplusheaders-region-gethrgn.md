---
UID: NF:gdiplusheaders.Region.GetHRGN
title: Region::GetHRGN (gdiplusheaders.h)
description: The Region::GetHRGN method creates a Windows Graphics Device Interface (GDI) region from this region.
helpviewer_keywords: ["GetHRGN","GetHRGN method [GDI+]","GetHRGN method [GDI+]","Region class","Region class [GDI+]","GetHRGN method","Region.GetHRGN","Region::GetHRGN","_gdiplus_CLASS_Region_GetHRGN_g_","gdiplus._gdiplus_CLASS_Region_GetHRGN_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_GetHRGN_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\gethrgn.htm
ms.date: 12/05/2018
ms.keywords: GetHRGN, GetHRGN method [GDI+], GetHRGN method [GDI+],Region class, Region class [GDI+],GetHRGN method, Region.GetHRGN, Region::GetHRGN, _gdiplus_CLASS_Region_GetHRGN_g_, gdiplus._gdiplus_CLASS_Region_GetHRGN_g_
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
 - Region::GetHRGN
 - gdiplusheaders/Region::GetHRGN
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
 - Region.GetHRGN
---

# Region::GetHRGN


## -description

The <b>Region::GetHRGN</b> method creates a Windows Graphics Device Interface (GDI) region from this region.

## -parameters

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region.

## -returns

Type: <b>HRGN</b>

This method returns a Windows handle to a GDI region that is created from this region.

## -remarks

It is the caller's responsibility to call the GDI function 
				<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> to free the GDI region when it is no longer needed.


#### Examples



The following example creates a GDI+ region from a path and then uses the GDI+ region to create a GDI region. The code then uses a GDI function to display the GDI region.


```cpp
VOID Example_GetHRGN(HDC hdc)
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
   path.AddClosedCurve(points, 6);

    // Create a region from a path.
    Region pathRegion(&path);

   // Get a handle to a GDI region.
   HRGN hRegion;
   hRegion = pathRegion.GetHRGN(&graphics);

   // Use GDI to display the region.
   HBRUSH hBrush = CreateSolidBrush(RGB(255, 0, 0));
   FillRgn(hdc, hRegion, hBrush);

   DeleteObject(hBrush);
   DeleteObject(hRegion);
}
```

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>