---
UID: NF:gdiplusgraphics.Graphics.FillEllipse(IN const Brush,IN INT,IN INT,IN INT,IN INT)
title: Graphics::FillEllipse(IN const Brush,IN INT,IN INT,IN INT,IN INT) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::FillEllipse method uses a brush to fill the interior of an ellipse that is specified by coordinates and dimensions.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_INT_x_INT_y_INT_width_INT_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillellipsemethods\fillellipse_85brushbrush_intx_inty_intwidth_intheigh.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FillEllipse, FillEllipse method [GDI+], FillEllipse method [GDI+],Graphics class, Graphics class [GDI+],FillEllipse method, Graphics.FillEllipse, Graphics.FillEllipse(IN const Brush,IN INT,IN INT,IN INT,IN INT), Graphics.FillEllipse(const Brush*,INT,INT,INT,INT), Graphics::FillEllipse, Graphics::FillEllipse(IN const Brush,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_INT_x_INT_y_INT_width_INT_height_, gdiplus._gdiplus_CLASS_Graphics_FillEllipse_Brush_brush_INT_x_INT_y_INT_width_INT_height_
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillEllipse(IN const Brush,IN INT,IN INT,IN INT,IN INT)


## -description


The <b>Graphics::FillEllipse</b> method uses a brush to fill the interior of an ellipse that is specified by coordinates and dimensions.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object that is used to paint the interior of the ellipse. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle that specifies the boundaries of the ellipse. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle that specifies the boundaries of the ellipse. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle that specifies the boundaries of the ellipse. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle that specifies the boundaries of the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
 

 

