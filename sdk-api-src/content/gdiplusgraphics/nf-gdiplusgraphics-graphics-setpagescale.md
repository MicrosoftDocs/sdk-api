---
UID: NF:gdiplusgraphics.Graphics.SetPageScale
title: Graphics::SetPageScale
author: windows-sdk-content
description: The Graphics::SetPageScale method sets the scaling factor for the page transformation of this Graphics object. The page transformation converts page coordinates to device coordinates.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetPageScale_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setpagescale.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Graphics class [GDI+],SetPageScale method, Graphics.SetPageScale, Graphics::SetPageScale, SetPageScale, SetPageScale method [GDI+], SetPageScale method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetPageScale_scale_, gdiplus._gdiplus_CLASS_Graphics_SetPageScale_scale_
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
 - Graphics.SetPageScale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetPageScale


## -description


The <b>Graphics::SetPageScale</b> method sets the scaling factor for the page transformation of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The page transformation converts page coordinates to device coordinates.


## -parameters




### -param scale [in]

Type: <b>REAL</b>

Real number that specifies the scaling factor. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535703(v=VS.85).aspx">Graphics::GetDpiX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535705(v=VS.85).aspx">Graphics::GetDpiY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535716(v=VS.85).aspx">Graphics::GetPageScale</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535718(v=VS.85).aspx">Graphics::GetPageUnit</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535812(v=VS.85).aspx">Graphics::SetPageUnit</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536399(v=VS.85).aspx">Types of Coordinate Systems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a>
 

 

