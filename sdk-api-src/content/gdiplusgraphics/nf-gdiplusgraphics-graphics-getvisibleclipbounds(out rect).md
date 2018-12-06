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
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this 
			<b>Graphics</b> object and the clipping region of the window.


## -parameters




### -param rect [out]

Type: <b>Rect*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the rectangle that encloses the visible clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/b46ce1d3-c2b5-4dbf-86b7-2e6f52ab2787">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/73733baf-6cbf-4220-b89d-0cd6856acc46">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/35425397-49b2-4388-a99f-a80b0b2027dc">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

