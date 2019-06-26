---
UID: NF:gdiplusgraphics.Graphics.SetPageUnit
title: Graphics::SetPageUnit (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetPageUnit method sets the unit of measure for this Graphics object. The page unit belongs to the page transformation, which converts page coordinates to device coordinates.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetPageUnit_unit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setpageunit.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetPageUnit method, Graphics.SetPageUnit, Graphics::SetPageUnit, SetPageUnit, SetPageUnit method [GDI+], SetPageUnit method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetPageUnit_unit_, gdiplus._gdiplus_CLASS_Graphics_SetPageUnit_unit_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.SetPageUnit"
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
 - Graphics.SetPageUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::SetPageUnit


## -description


The <b>Graphics::SetPageUnit</b> method sets the unit of measure for this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The page unit belongs to the page transformation, which converts page coordinates to device coordinates.


## -parameters




### -param unit [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix">Graphics::GetDpiX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy">Graphics::GetDpiY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale">Graphics::GetPageScale</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit">Graphics::GetPageUnit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale">Graphics::SetPageScale</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-types-of-coordinate-systems-about">Types of Coordinate Systems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>
 

 

