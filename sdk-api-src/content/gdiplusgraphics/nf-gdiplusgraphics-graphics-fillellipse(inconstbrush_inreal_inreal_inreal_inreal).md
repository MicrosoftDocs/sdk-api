---
UID: NF:gdiplusgraphics.Graphics.FillEllipse(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL)
title: Graphics::FillEllipse(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::FillEllipse method uses a brush to fill the interior of an ellipse that is specified by coordinates and dimensions.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillellipsemethods\fillellipse_53brushbrush_realx_realy_realwidth_realh.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FillEllipse, FillEllipse method [GDI+], FillEllipse method [GDI+],Graphics class, Graphics class [GDI+],FillEllipse method, Graphics.FillEllipse, Graphics.FillEllipse(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.FillEllipse(const Brush*,REAL,REAL,REAL,REAL), Graphics::FillEllipse, Graphics::FillEllipse(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_, gdiplus._gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.FillEllipse"
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
 - Graphics.FillEllipse
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::FillEllipse(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>Graphics::FillEllipse</b> method uses a brush to fill the interior of an ellipse that is specified by coordinates and dimensions.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a brush that is used to paint the interior of the ellipse. 


### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that specifies the boundaries of the ellipse. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that specifies the boundaries of the ellipse. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that specifies the boundaries of the ellipse. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that specifies the boundaries of the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>
 

 

