---
UID: NF:gdiplusgraphics.Graphics.SetSmoothingMode
title: Graphics::SetSmoothingMode (gdiplusgraphics.h)
description: The Graphics::SetSmoothingMode method sets the rendering quality of the Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","SetSmoothingMode method","Graphics.SetSmoothingMode","Graphics::SetSmoothingMode","SetSmoothingMode","SetSmoothingMode method [GDI+]","SetSmoothingMode method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_","gdiplus._gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setsmoothingmode.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetSmoothingMode method, Graphics.SetSmoothingMode, Graphics::SetSmoothingMode, SetSmoothingMode, SetSmoothingMode method [GDI+], SetSmoothingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_, gdiplus._gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_
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
 - Graphics::SetSmoothingMode
 - gdiplusgraphics/Graphics::SetSmoothingMode
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
 - Graphics.SetSmoothingMode
---

# Graphics::SetSmoothingMode


## -description

The <b>Graphics::SetSmoothingMode</b> method sets the rendering quality of the <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param smoothingMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-smoothingmode">SmoothingMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-smoothingmode">SmoothingMode</a> enumeration that specifies whether smoothing (antialiasing) is applied to lines and curves.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

To get the rendering quality for text, use the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettextrenderinghint">Graphics::GetTextRenderingHint</a> method. The higher the level of quality of the smoothing mode, the slower the performance.


#### Examples



The following example sets the smoothing mode to two different values and fills an ellipse to demonstrate each mode.


```cpp
VOID Example_SetSetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);
   graphics.FillEllipse(&SolidBrush(Color(255, 0, 0, 0)), 0, 0, 200, 100);

   // Set the smoothing mode to SmoothingModeHighQuality, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.FillEllipse(&SolidBrush(Color(255, 0, 0, 0)), 200, 0, 200, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-antialiasing-with-lines-and-curves-about">Antialiasing with Lines and Curves</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getsmoothingmode">Graphics::GetSmoothingMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>