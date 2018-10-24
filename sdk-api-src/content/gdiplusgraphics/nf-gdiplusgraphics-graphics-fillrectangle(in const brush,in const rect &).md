---
UID: NF:gdiplusgraphics.Graphics.FillRectangle(IN const Brush,IN const Rect &)
title: Graphics::FillRectangle(IN const Brush,IN const Rect &)
author: windows-sdk-content
description: The Graphics::FillRectangle method uses a brush to fill the interior of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillrectanglemethods\fillrectangle.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FillRectangle, FillRectangle method [GDI+], FillRectangle method [GDI+],Graphics class, Graphics class [GDI+],FillRectangle method, Graphics.FillRectangle, Graphics.FillRectangle(IN const Brush,IN const Rect &), Graphics.FillRectangle(const Brush*,const Rect&), Graphics::FillRectangle, Graphics::FillRectangle(IN const Brush,IN const Rect &), _gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_Rect_rect_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Graphics.FillRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillRectangle(IN const Brush,IN const Rect &)


## -description


The <b>Graphics::FillRectangle</b> method uses a brush to fill the interior of a rectangle.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> that is used to paint the interior of the rectangle. 


### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to the rectangle to be filled. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

