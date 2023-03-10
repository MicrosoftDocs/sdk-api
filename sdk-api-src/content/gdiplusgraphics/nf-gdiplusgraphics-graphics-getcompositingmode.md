---
UID: NF:gdiplusgraphics.Graphics.GetCompositingMode
title: Graphics::GetCompositingMode (gdiplusgraphics.h)
description: The Graphics::GetCompositingMode method gets the compositing mode currently set for this Graphics object.
helpviewer_keywords: ["GetCompositingMode","GetCompositingMode method [GDI+]","GetCompositingMode method [GDI+]","Graphics class","Graphics class [GDI+]","GetCompositingMode method","Graphics.GetCompositingMode","Graphics::GetCompositingMode","_gdiplus_CLASS_Graphics_GetCompositingMode_","gdiplus._gdiplus_CLASS_Graphics_GetCompositingMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetCompositingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getcompositingmode.htm
ms.date: 12/05/2018
ms.keywords: GetCompositingMode, GetCompositingMode method [GDI+], GetCompositingMode method [GDI+],Graphics class, Graphics class [GDI+],GetCompositingMode method, Graphics.GetCompositingMode, Graphics::GetCompositingMode, _gdiplus_CLASS_Graphics_GetCompositingMode_, gdiplus._gdiplus_CLASS_Graphics_GetCompositingMode_
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
 - Graphics::GetCompositingMode
 - gdiplusgraphics/Graphics::GetCompositingMode
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
 - Graphics.GetCompositingMode
---

# Graphics::GetCompositingMode


## -description

The <b>Graphics::GetCompositingMode</b> method gets the compositing mode currently set for this 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingmode">CompositingMode</a></b>

This method returns an element of the 
						<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingmode">CompositingMode</a> enumeration that indicates the compositing mode currently set for this 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -remarks

Suppose you create a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object based on a color that has an alpha component of 192, which is about 75 percent of 255. If your 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object has its compositing mode set to CompositingModeSourceOver, then areas filled with the solid brush are a blend that is 75 percent brush color and 25 percent background color. If your 
				<b>Graphics</b> object has its compositing mode set to CompositingModeSourceCopy, then the background color is not blended with the brush color. However, the color rendered by the brush has an intensity that is 75 percent of what it would be if the alpha component were 255.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and sets its compositing mode to CompositingModeSourceCopy. The code creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object based on a color with an alpha component of 128. The code passes the address of that brush to the
<a href="/previous-versions/ms535957(v=vs.85)">Graphics::FillRectangle</a> method of the 
						<b>Graphics</b> object to fill a rectangle with a color that is not blended with the background color. The call to the <b>Graphics::GetCompositingMode</b> method of the 
						<b>Graphics</b> object demonstrates how to obtain the compositing mode (which is already known in this case). The code determines whether the compositing mode is CompositingModeSourceCopy and if so, changes it to CompositingModeSourceOver. Then the code calls 
						<b>Graphics::FillRectangle</b> a second time to fill a rectangle with a color that is a half-and-half blend of the brush color and the background color.


```cpp
VOID Example_GetCompositingMode(HDC hdc)
{
   Graphics graphics(hdc);
   
   graphics.SetCompositingMode(CompositingModeSourceCopy);
   SolidBrush alphaBrush(Color(128, 255, 0, 0));
   graphics.FillRectangle(&alphaBrush, 0, 0, 100, 100);
   
   // Get the compositing mode.
   CompositingMode compMode = graphics.GetCompositingMode();
   
   // Change the compositing mode if it is CompositingModeSourceCopy.
   if(compMode == CompositingModeSourceCopy)
   {
      graphics.SetCompositingMode(CompositingModeSourceOver);
   }  
  
   graphics.FillRectangle(&alphaBrush, 0, 100, 100, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-alpha-blending-lines-and-fills-use">Alpha Blending Lines and Fills</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingquality">Graphics::GetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode">Graphics::SetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality">Graphics::SetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-new-features-about">New Features</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-compositing-mode-to-control-alpha-blending-use">Using Compositing Mode to Control Alpha Blending</a>
