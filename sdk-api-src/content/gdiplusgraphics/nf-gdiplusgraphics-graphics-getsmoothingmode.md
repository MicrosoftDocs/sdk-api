---
UID: NF:gdiplusgraphics.Graphics.GetSmoothingMode
title: Graphics::GetSmoothingMode (gdiplusgraphics.h)
description: The Graphics::GetSmoothingMode method determines whether smoothing (antialiasing) is applied to the Graphics object.
helpviewer_keywords: ["GetSmoothingMode","GetSmoothingMode method [GDI+]","GetSmoothingMode method [GDI+]","Graphics class","Graphics class [GDI+]","GetSmoothingMode method","Graphics.GetSmoothingMode","Graphics::GetSmoothingMode","_gdiplus_CLASS_Graphics_GetSmoothingMode_","gdiplus._gdiplus_CLASS_Graphics_GetSmoothingMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetSmoothingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getsmoothingmode.htm
ms.date: 12/05/2018
ms.keywords: GetSmoothingMode, GetSmoothingMode method [GDI+], GetSmoothingMode method [GDI+],Graphics class, Graphics class [GDI+],GetSmoothingMode method, Graphics.GetSmoothingMode, Graphics::GetSmoothingMode, _gdiplus_CLASS_Graphics_GetSmoothingMode_, gdiplus._gdiplus_CLASS_Graphics_GetSmoothingMode_
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
 - Graphics::GetSmoothingMode
 - gdiplusgraphics/Graphics::GetSmoothingMode
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
 - Graphics.GetSmoothingMode
---

# Graphics::GetSmoothingMode


## -description

The <b>Graphics::GetSmoothingMode</b> method determines whether smoothing (antialiasing) is applied to the 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-smoothingmode">SmoothingMode</a></b>

If smoothing (antialiasing) is applied to this 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, this method returns SmoothingModeAntiAlias. If smoothing (antialiasing) is not applied to this 
						<b>Graphics</b> object, this method returns SmoothingModeNone. SmoothingModeAntiAlias and SmoothingModeNone are elements of the 
						<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-smoothingmode">SmoothingMode</a> enumeration.

## -remarks

To get the rendering quality level for text, use the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gettextrenderinghint">Graphics::GetTextRenderingHint</a> method.


#### Examples



The following example sets the smoothing mode to high speed and draws an ellipse. It then gets the smoothing mode, changes it to high quality, and draws a second ellipse to demonstrate the difference.


```cpp
VOID Example_GetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);

   // Draw an ellipse.
   graphics.DrawEllipse(&Pen(Color(255, 0, 0, 0), 3), Rect(10, 0, 200, 100));

   // Get the smoothing mode.
   SmoothingMode mode = graphics.GetSmoothingMode();


   // Test mode to see whether smoothing has been set for the Graphics object.
   if (mode == SmoothingModeAntiAlias)
   {
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   }

   // Draw an ellipse to demonstrate the difference.
   graphics.DrawEllipse(&Pen(Color::Red, 3), Rect(220, 0, 200, 100));
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-antialiasing-with-lines-and-curves-about">Antialiasing with Lines and Curves</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>
