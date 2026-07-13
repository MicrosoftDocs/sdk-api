---
UID: NF:gdiplusgraphics.Graphics.IsVisible(constPoint&)
title: Graphics::IsVisible(IN const Point &) (gdiplusgraphics.h)
description: The Graphics::IsVisible method determines whether the specified point is inside the visible clipping region of this Graphics object. (overload 2/4)
helpviewer_keywords: ["Graphics class [GDI+]","IsVisible method","Graphics.IsVisible","Graphics.IsVisible(IN const Point &)","Graphics.IsVisible(const Point&)","Graphics::IsVisible","Graphics::IsVisible(IN const Point &)","IsVisible","IsVisible method [GDI+]","IsVisible method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_IsVisible_Point_point_","gdiplus._gdiplus_CLASS_Graphics_IsVisible_Point_point_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisible_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsisvisiblemethods\isvisible.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],IsVisible method, Graphics.IsVisible, Graphics.IsVisible(IN const Point &), Graphics.IsVisible(const Point&), Graphics::IsVisible, Graphics::IsVisible(IN const Point &), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsVisible_Point_point_, gdiplus._gdiplus_CLASS_Graphics_IsVisible_Point_point_
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
 - Graphics::IsVisible
 - gdiplusgraphics/Graphics::IsVisible
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
 - Graphics.IsVisible
---

# Graphics::IsVisible(IN const Point &)


## -description

The <b>Graphics::IsVisible</b> method determines whether the specified point is inside the visible clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

## -parameters

### -param point [in]

Type: <b>const Point&amp;</b>

Reference to a point to be tested to see whether it is inside the visible clipping region.

## -returns

Type: <b>BOOL</b>

If the specified point is inside the visible clipping region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
