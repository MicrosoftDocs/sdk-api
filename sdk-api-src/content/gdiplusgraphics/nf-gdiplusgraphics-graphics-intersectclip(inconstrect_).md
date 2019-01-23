---
UID: NF:gdiplusgraphics.Graphics.IntersectClip(IN const Rect &)
title: Graphics::IntersectClip(IN const Rect &)
author: windows-sdk-content
description: The Graphics::IntersectClip method updates the clipping region of this Graphics object to the portion of the specified rectangle that intersects with the current clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IntersectClip_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsintersectclipmethods\intersectclip.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics class [GDI+],IntersectClip method, Graphics.IntersectClip, Graphics.IntersectClip(IN const Rect &), Graphics.IntersectClip(const Rect&), Graphics::IntersectClip, Graphics::IntersectClip(IN const Rect &), IntersectClip, IntersectClip method [GDI+], IntersectClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IntersectClip_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_IntersectClip_Rect_rect_
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
 - Graphics.IntersectClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::IntersectClip(IN const Rect &)


## -description


The <b>Graphics::IntersectClip</b> method updates the clipping region of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to the portion of the specified rectangle that intersects with the current clipping region of this 
			<b>Graphics</b> object.


## -parameters




### -param rect [in]

Type: <b>const Rect&amp;</b>

Reference to a rectangle that is used to update the clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

