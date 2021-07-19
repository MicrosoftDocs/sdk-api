---
UID: NF:gdiplusgraphics.Graphics.GetInterpolationMode
title: Graphics::GetInterpolationMode (gdiplusgraphics.h)
description: The Graphics::GetInterpolationMode method gets the interpolation mode currently set for this Graphics object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.
helpviewer_keywords: ["GetInterpolationMode","GetInterpolationMode method [GDI+]","GetInterpolationMode method [GDI+]","Graphics class","Graphics class [GDI+]","GetInterpolationMode method","Graphics.GetInterpolationMode","Graphics::GetInterpolationMode","_gdiplus_CLASS_Graphics_GetInterpolationMode_","gdiplus._gdiplus_CLASS_Graphics_GetInterpolationMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetInterpolationMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getinterpolationmode.htm
ms.date: 12/05/2018
ms.keywords: GetInterpolationMode, GetInterpolationMode method [GDI+], GetInterpolationMode method [GDI+],Graphics class, Graphics class [GDI+],GetInterpolationMode method, Graphics.GetInterpolationMode, Graphics::GetInterpolationMode, _gdiplus_CLASS_Graphics_GetInterpolationMode_, gdiplus._gdiplus_CLASS_Graphics_GetInterpolationMode_
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
 - Graphics::GetInterpolationMode
 - gdiplusgraphics/Graphics::GetInterpolationMode
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
 - Graphics.GetInterpolationMode
---

# Graphics::GetInterpolationMode


## -description

The <b>Graphics::GetInterpolationMode</b> method gets the interpolation mode currently set for this 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a></b>

This method returns an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a> enumeration that indicates the interpolation mode currently set for this 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode">Graphics::SetInterpolationMode</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use">Using Interpolation Mode to Control Image Quality During Scaling</a>
