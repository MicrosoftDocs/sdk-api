---
UID: NF:gdiplusgraphics.Graphics.FillRectangle(IN const Brush,IN INT,IN INT,IN INT,IN INT)
title: Graphics::FillRectangle(IN const Brush,IN INT,IN INT,IN INT,IN INT) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::FillRectangle method uses a brush to fill the interior of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_INT_x_INT_y_INT_width_INT_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillrectanglemethods\fillrectangle_79brushbrush_intx_inty_intwidth_intheigh.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FillRectangle, FillRectangle method [GDI+], FillRectangle method [GDI+],Graphics class, Graphics class [GDI+],FillRectangle method, Graphics.FillRectangle, Graphics.FillRectangle(IN const Brush,IN INT,IN INT,IN INT,IN INT), Graphics.FillRectangle(const Brush*,INT,INT,INT,INT), Graphics::FillRectangle, Graphics::FillRectangle(IN const Brush,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_INT_x_INT_y_INT_width_INT_height_, gdiplus._gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_INT_x_INT_y_INT_width_INT_height_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.FillRectangle"
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
 - Graphics.FillRectangle
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::FillRectangle(IN const Brush,IN INT,IN INT,IN INT,IN INT)


## -description


The <b>Graphics::FillRectangle</b> method uses a brush to fill the interior of a rectangle. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> that is used to paint the interior of the rectangle. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle to be filled. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle to be filled. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle to be filled. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle to be filled. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

