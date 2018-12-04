---
UID: NF:gdiplusgraphics.Graphics.GetRenderingOrigin
title: Graphics::GetRenderingOrigin
author: windows-sdk-content
description: The Graphics::GetRenderingOrigin method gets the rendering origin currently set for this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetRenderingOrigin_x_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getrenderingorigin.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetRenderingOrigin, GetRenderingOrigin method [GDI+], GetRenderingOrigin method [GDI+],Graphics class, Graphics class [GDI+],GetRenderingOrigin method, Graphics.GetRenderingOrigin, Graphics::GetRenderingOrigin, _gdiplus_CLASS_Graphics_GetRenderingOrigin_x_y_, gdiplus._gdiplus_CLASS_Graphics_GetRenderingOrigin_x_y_
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
 - Graphics.GetRenderingOrigin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetRenderingOrigin


## -description


The <b>Graphics::GetRenderingOrigin</b> method gets the rendering origin currently set for this 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The rendering origin is used to set the dither origin for 8-bits per pixel and 16-bits per pixel dithering and is also used to set the origin for hatch brushes.


## -parameters




### -param x [out]

Type: <b>INT*</b>

Pointer to an 
					<b>INT</b> that receives the x-coordinate of the rendering origin. 


### -param y [out]

Type: <b>INT*</b>

Pointer to an 
					<b>INT</b> that receives the y-coordinate of the rendering origin. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/2e568966-8f37-460a-8715-76e67593001b">Graphics::SetRenderingOrigin</a>
 

 

