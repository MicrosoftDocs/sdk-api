---
UID: NF:gdiplusgraphics.Graphics.DrawPath
title: Graphics::DrawPath
author: windows-sdk-content
description: The Graphics::DrawPath method draws a sequence of lines and curves defined by a GraphicsPath object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPath_pen_path_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawpath.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DrawPath, DrawPath method [GDI+], DrawPath method [GDI+],Graphics class, Graphics class [GDI+],DrawPath method, Graphics.DrawPath, Graphics::DrawPath, _gdiplus_CLASS_Graphics_DrawPath_pen_path_, gdiplus._gdiplus_CLASS_Graphics_DrawPath_pen_path_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::DrawPath


## -description


The <b>Graphics::DrawPath</b> method draws a sequence of lines and curves defined by a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the path. 


### -param path [in]

Type: <b>const <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object that specifies the sequence of lines and curves that make up the path. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/66faeb73-16fb-4b7f-a4d5-a90ec2590d8c">Creating Figures from Lines, Curves, and Shapes</a>



<a href="https://msdn.microsoft.com/e6de6634-b87f-4fe9-a0d4-ffeea0e0ae8b">FillPie Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

