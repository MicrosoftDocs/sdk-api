---
UID: NF:gdiplusgraphics.Graphics.SetInterpolationMode
title: Graphics::SetInterpolationMode (gdiplusgraphics.h)
description: The Graphics::SetInterpolationMode method sets the interpolation mode of this Graphics object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.
helpviewer_keywords: ["Graphics class [GDI+]","SetInterpolationMode method","Graphics.SetInterpolationMode","Graphics::SetInterpolationMode","SetInterpolationMode","SetInterpolationMode method [GDI+]","SetInterpolationMode method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_","gdiplus._gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setinterpolationmode.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetInterpolationMode method, Graphics.SetInterpolationMode, Graphics::SetInterpolationMode, SetInterpolationMode, SetInterpolationMode method [GDI+], SetInterpolationMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_, gdiplus._gdiplus_CLASS_Graphics_SetInterpolationMode_interpolationMode_
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
 - Graphics::SetInterpolationMode
 - gdiplusgraphics/Graphics::SetInterpolationMode
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
 - Graphics.SetInterpolationMode
---

# Graphics::SetInterpolationMode


## -description

The <b>Graphics::SetInterpolationMode</b> method sets the interpolation mode of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The interpolation mode determines the algorithm that is used when images are scaled or rotated.

## -parameters

### -param interpolationMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a> enumeration that specifies the interpolation mode.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getinterpolationmode">Graphics::GetInterpolationMode</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use">Using Interpolation Mode to Control Image Quality During Scaling</a>