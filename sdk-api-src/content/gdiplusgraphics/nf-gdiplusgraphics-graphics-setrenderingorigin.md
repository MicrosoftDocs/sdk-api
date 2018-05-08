---
UID: NF:gdiplusgraphics.Graphics.SetRenderingOrigin
title: Graphics::SetRenderingOrigin
author: windows-driver-content
description: The Graphics::SetRenderingOrigin method sets the rendering origin of this Graphics object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setrenderingorigin.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Graphics class [GDI+],SetRenderingOrigin method, Graphics.SetRenderingOrigin, Graphics::SetRenderingOrigin, SetRenderingOrigin, SetRenderingOrigin method [GDI+], SetRenderingOrigin method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_, gdiplus._gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.SetRenderingOrigin
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::SetRenderingOrigin


## -description


The <b>Graphics::SetRenderingOrigin</b> method sets the rendering origin of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the rendering origin. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the rendering origin. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/373beeb6-bc92-41fc-8bb2-83ac11ca24ab">Graphics::GetRenderingOrigin</a>
 

 

