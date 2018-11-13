---
UID: NF:gdiplusgraphics.Graphics.DrawPath
title: Graphics::DrawPath
author: windows-sdk-content
description: The Graphics::DrawPath method draws a sequence of lines and curves defined by a GraphicsPath object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPath_pen_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawpath.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawPath, DrawPath method [GDI+], DrawPath method [GDI+],Graphics class, Graphics class [GDI+],DrawPath method, Graphics.DrawPath, Graphics::DrawPath, _gdiplus_CLASS_Graphics_DrawPath_pen_path_, gdiplus._gdiplus_CLASS_Graphics_DrawPath_pen_path_
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
 - Graphics.DrawPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawPath


## -description


The <b>Graphics::DrawPath</b> method draws a sequence of lines and curves defined by a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the path. 


### -param path [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object that specifies the sequence of lines and curves that make up the path. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533919(v=VS.85).aspx">Creating Figures from Lines, Curves, and Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535769(v=VS.85).aspx">FillPie Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

