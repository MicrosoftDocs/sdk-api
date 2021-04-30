---
UID: NF:gdiplusgraphics.Graphics.FillRegion
title: Graphics::FillRegion (gdiplusgraphics.h)
description: The Graphics::FillRegion method uses a brush to fill a specified region.
helpviewer_keywords: ["FillRegion","FillRegion method [GDI+]","FillRegion method [GDI+]","Graphics class","Graphics class [GDI+]","FillRegion method","Graphics.FillRegion","Graphics::FillRegion","_gdiplus_CLASS_Graphics_FillRegion_brush_region_","gdiplus._gdiplus_CLASS_Graphics_FillRegion_brush_region_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRegion_brush_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fillregion.htm
ms.date: 12/05/2018
ms.keywords: FillRegion, FillRegion method [GDI+], FillRegion method [GDI+],Graphics class, Graphics class [GDI+],FillRegion method, Graphics.FillRegion, Graphics::FillRegion, _gdiplus_CLASS_Graphics_FillRegion_brush_region_, gdiplus._gdiplus_CLASS_Graphics_FillRegion_brush_region_
req.header: gdiplusgraphics.h
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
 - Graphics::FillRegion
 - gdiplusgraphics/Graphics::FillRegion
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
 - Graphics.FillRegion
---

# Graphics::FillRegion


## -description

The <b>Graphics::FillRegion</b> method uses a brush to fill a specified region.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a brush that is used to paint the region.

### -param region [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to a region to be filled.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Because a region describes a set of pixels, a pixel is considered either fully inside, or fully outside the region. Consequently, <b>Graphics::FillRegion</b> does not antialias the edges of the region.


#### Examples



The following example creates a region from a rectangle and then fills the region.


```cpp
VOID Example_FillRegion(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create a Region object from a rectangle.
   Region ellipseRegion(Rect(0, 0, 200, 100));

   // Fill the region.
   graphics.FillRegion(&blackBrush, &ellipseRegion);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-regions-about">Regions</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>