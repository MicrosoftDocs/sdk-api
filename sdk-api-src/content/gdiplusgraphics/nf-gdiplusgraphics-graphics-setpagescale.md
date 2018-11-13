---
UID: NF:gdiplusgraphics.Graphics.SetPageScale
title: Graphics::SetPageScale
author: windows-sdk-content
description: The Graphics::SetPageScale method sets the scaling factor for the page transformation of this Graphics object. The page transformation converts page coordinates to device coordinates.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetPageScale_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setpagescale.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
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


The <b>Graphics::SetPageScale</b> method sets the scaling factor for the page transformation of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The page transformation converts page coordinates to device coordinates.


## -parameters




### -param scale [in]

Type: <b>REAL</b>

Real number that specifies the scaling factor. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/66b2afd6-5cba-4eab-a2ec-234bacb9d636">Graphics::GetDpiX</a>



<a href="https://msdn.microsoft.com/85925de9-c5a8-4fc4-b6ef-e1716c548dac">Graphics::GetDpiY</a>



<a href="https://msdn.microsoft.com/effda356-1e87-41e0-bb55-1e674b459b88">Graphics::GetPageScale</a>



<a href="https://msdn.microsoft.com/1fdac4c0-4494-4e15-8d8b-e9e54cbcad6c">Graphics::GetPageUnit</a>



<a href="https://msdn.microsoft.com/f931ac83-df22-426b-9323-7c0857903410">Graphics::SetPageUnit</a>



<a href="https://msdn.microsoft.com/eb20f5e9-25f5-4f27-8ea5-83f6819425ed">Types of Coordinate Systems</a>



<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a>
 

 

