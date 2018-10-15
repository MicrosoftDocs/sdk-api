---
UID: NF:gdipluspath.GraphicsPath.SetFillMode
title: GraphicsPath::SetFillMode
author: windows-sdk-content
description: The GraphicsPath::SetFillMode method sets the fill mode of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\setfillmode.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GraphicsPath class [GDI+],SetFillMode method, GraphicsPath.SetFillMode, GraphicsPath::SetFillMode, SetFillMode, SetFillMode method [GDI+], SetFillMode method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_, gdiplus._gdiplus_CLASS_GraphicsPath_SetFillMode_fillmode_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::SetFillMode


## -description


The <b>GraphicsPath::SetFillMode</b> method sets the fill mode of this path.


## -parameters




### -param fillmode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a> enumeration that specifies how to fill areas when the path intersects itself. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534120(v=VS.85).aspx">FillMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

