---
UID: NF:gdiplusgraphics.Graphics.SetCompositingMode
title: Graphics::SetCompositingMode (gdiplusgraphics.h)
description: The Graphics::SetCompositingMode method sets the compositing mode of this Graphics object.
helpviewer_keywords: ["Graphics class [GDI+]","SetCompositingMode method","Graphics.SetCompositingMode","Graphics::SetCompositingMode","SetCompositingMode","SetCompositingMode method [GDI+]","SetCompositingMode method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_","gdiplus._gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setcompositingmode.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetCompositingMode method, Graphics.SetCompositingMode, Graphics::SetCompositingMode, SetCompositingMode, SetCompositingMode method [GDI+], SetCompositingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_, gdiplus._gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_
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
 - Graphics::SetCompositingMode
 - gdiplusgraphics/Graphics::SetCompositingMode
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
 - Graphics.SetCompositingMode
---

# Graphics::SetCompositingMode


## -description

The <b>Graphics::SetCompositingMode</b> method sets the compositing mode of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param compositingMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingmode">CompositingMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingmode">CompositingMode</a> enumeration that specifies the compositing mode.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Suppose you create a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object based on a color that has an alpha component of 192, which is about 75 percent of 255. If your <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object has its compositing mode set to CompositingModeSourceOver, then areas filled with the solid brush are a blend that is 75 percent brush color and 25 percent background color. If your <b>Graphics</b> object has its compositing mode set to CompositingModeSourceCopy, then the background color is not blended with the brush color. However, the color rendered by the brush has an intensity that is 75 percent of what it would be if the alpha component were 255.

You cannot use CompositingModeSourceCopy along with TextRenderingHintClearTypeGridFit.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and sets its compositing mode to CompositingModeSourceOver. The code creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object based on a color that has an alpha component of 128. The code passes the address of that brush to the <a href="/previous-versions/ms535954(v=vs.85)">Graphics::FillRectangle</a> method of the <b>Graphics</b> object to fill a rectangle with a color that is a half-and-half blend of the brush color and the background color. Then the code sets the compositing mode of the <b>Graphics</b> object to CompositingModeSourceCopy and fills a second rectangle with the same brush. In that second rectangle, the brush color is not blended with the background color.


```cpp
VOID Example_SetCompositingMode(HDC hdc)
{
   Graphics graphics(hdc);
   
   // Create a SolidBrush object with an alpha-blended color.
   SolidBrush alphaBrush(Color(180, 255, 0, 0));

   // Set the compositing mode to CompositingModeSourceOver,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceOver);
   graphics.FillRectangle(&alphaBrush, 0, 0, 100, 100);

   // Set the compositing mode to CompositingModeSourceCopy,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceCopy);
   graphics.FillRectangle(&alphaBrush, 100, 0, 100, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-alpha-blending-lines-and-fills-use">Alpha Blending Lines and Fills</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-compositingmode">CompositingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingmode">Graphics::GetCompositingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingquality">Graphics::GetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality">Graphics::SetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint">Graphics::SetTextRenderingHint</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-new-features-about">New Features</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-textrenderinghint">TextRenderingHint</a>