---
UID: NF:gdipluspath.GraphicsPath.SetFillMode
title: GraphicsPath::SetFillMode (gdipluspath.h)

description: The GraphicsPath::SetFillMode method sets the fill mode of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\setfillmode.htm

ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],SetFillMode method, GraphicsPath.SetFillMode, GraphicsPath::SetFillMode, SetFillMode, SetFillMode method [GDI+], SetFillMode method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_, gdiplus._gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_
ms.topic: method
f1_keywords: 
 - "gdipluspath/GraphicsPath.SetFillMode"
dev_langs:
 - c++
req.header: gdipluspath.h
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
 - GraphicsPath.SetFillMode
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::SetFillMode


## -description


The <b>GraphicsPath::SetFillMode</b> method sets the fill mode of this path.


## -parameters




### -param fillmode [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a> enumeration that specifies how to fill areas when the path intersects itself. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
 

 

