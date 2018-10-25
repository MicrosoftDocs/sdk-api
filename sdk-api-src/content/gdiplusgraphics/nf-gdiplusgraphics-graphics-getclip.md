---
UID: NF:gdiplusgraphics.Graphics.GetClip
title: Graphics::GetClip
author: windows-sdk-content
description: The Graphics::GetClip method gets the clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetClip_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getclip.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetClip, GetClip method [GDI+], GetClip method [GDI+],Graphics class, Graphics class [GDI+],GetClip method, Graphics.GetClip, Graphics::GetClip, _gdiplus_CLASS_Graphics_GetClip_region_, gdiplus._gdiplus_CLASS_Graphics_GetClip_region_
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
 - Graphics.GetClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetClip


## -description


The <b>Graphics::GetClip</b> method gets the clipping region of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param region [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a> object that receives the clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method
fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535802(v=VS.85).aspx">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>
 

 

