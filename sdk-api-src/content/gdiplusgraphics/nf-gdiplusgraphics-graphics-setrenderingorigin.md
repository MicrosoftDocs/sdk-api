---
UID: NF:gdiplusgraphics.Graphics.SetRenderingOrigin
title: Graphics::SetRenderingOrigin (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetRenderingOrigin method sets the rendering origin of this Graphics object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setrenderingorigin.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetRenderingOrigin method, Graphics.SetRenderingOrigin, Graphics::SetRenderingOrigin, SetRenderingOrigin, SetRenderingOrigin method [GDI+], SetRenderingOrigin method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_, gdiplus._gdiplus_CLASS_Graphics_SetRenderingOrigin_x_y_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.SetRenderingOrigin"
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
 - Graphics.SetRenderingOrigin
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::SetRenderingOrigin


## -description


The <b>Graphics::SetRenderingOrigin</b> method sets the rendering origin of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The rendering origin is used to set the dither origin for 8-bits-per-pixel and 16-bits-per-pixel dithering and is also used to set the origin for hatch brushes.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the rendering origin. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the rendering origin. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getrenderingorigin">Graphics::GetRenderingOrigin</a>
 

 

