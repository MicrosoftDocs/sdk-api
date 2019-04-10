---
UID: NF:gdiplusgraphics.Graphics.DrawEllipse(IN const Pen,IN const Rect &)
title: Graphics::DrawEllipse(IN const Pen,IN const Rect &) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawEllipse method draws an ellipse.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawellipsemethods\drawellipse.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawEllipse, DrawEllipse method [GDI+], DrawEllipse method [GDI+],Graphics class, Graphics class [GDI+],DrawEllipse method, Graphics.DrawEllipse, Graphics.DrawEllipse(IN const Pen,IN const Rect &), Graphics.DrawEllipse(const Pen*,const Rect&), Graphics::DrawEllipse, Graphics::DrawEllipse(IN const Pen,IN const Rect &), _gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_
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
 - Graphics.DrawEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawEllipse(IN const Pen,IN const Rect &)


## -description


The <b>Graphics::DrawEllipse</b> method draws an ellipse.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the ellipse. 


### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a></b>

Reference to a rectangle that bounds the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535767(v=VS.85).aspx">FillEllipse Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>
 

 

