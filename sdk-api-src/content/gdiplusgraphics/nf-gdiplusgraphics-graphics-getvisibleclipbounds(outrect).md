---
UID: NF:gdiplusgraphics.Graphics.GetVisibleClipBounds(OUT Rect)
title: Graphics::GetVisibleClipBounds(OUT Rect)
author: windows-sdk-content
description: The Graphics::GetVisibleClipBounds method gets a rectangle that encloses the visible clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsgetvisibleclipboundsmethods\getvisibleclipbounds.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVisibleClipBounds, GetVisibleClipBounds method [GDI+], GetVisibleClipBounds method [GDI+],Graphics class, Graphics class [GDI+],GetVisibleClipBounds method, Graphics.GetVisibleClipBounds, Graphics.GetVisibleClipBounds(OUT Rect), Graphics.GetVisibleClipBounds(Rect*), Graphics::GetVisibleClipBounds, Graphics::GetVisibleClipBounds(OUT Rect), _gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_GetVisibleClipBounds_Rect_rect_
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
 - Graphics.GetVisibleClipBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetVisibleClipBounds(OUT Rect)


## -description


The <b>Graphics::GetVisibleClipBounds</b> method gets a rectangle that encloses the visible clipping region of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this 
			<b>Graphics</b> object and the clipping region of the window.


## -parameters




### -param rect [out]

Type: <b>Rect*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a> object that receives the rectangle that encloses the visible clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535794(v=VS.85).aspx">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535785(v=VS.85).aspx">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>
 

 

