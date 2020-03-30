---
UID: NF:gdiplusgraphics.Graphics.IsVisible(IN const RectF &)
title: Graphics::IsVisible(IN const RectF &) (gdiplusgraphics.h)
description: The Graphics::IsVisible method determines whether the specified rectangle intersects the visible clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisible_RectF_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsisvisiblemethods\isvisible_15rectfamprect.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],IsVisible method, Graphics.IsVisible, Graphics.IsVisible(IN const RectF &), Graphics.IsVisible(const RectF&), Graphics::IsVisible, Graphics::IsVisible(IN const RectF &), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsVisible_RectF_rect_, gdiplus._gdiplus_CLASS_Graphics_IsVisible_RectF_rect_
f1_keywords:
- gdiplusgraphics/Graphics.IsVisible
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Graphics.IsVisible
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::IsVisible(IN const RectF &)


## -description


The <b>Graphics::IsVisible</b> method determines whether the specified rectangle intersects the visible clipping region of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.


## -parameters




### -param rect [in]

Type: <b>const RectF&amp;</b>

Reference to a rectangle to be tested to see whether it intersects the visible clipping region. 


## -returns



Type: <b>BOOL</b>

If the specified rectangle intersects the visible clipping region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
 

 

