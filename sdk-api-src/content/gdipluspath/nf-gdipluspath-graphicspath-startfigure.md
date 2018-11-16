---
UID: NF:gdipluspath.GraphicsPath.StartFigure
title: GraphicsPath::StartFigure
author: windows-sdk-content
description: The GraphicsPath::StartFigure method starts a new figure without closing the current figure. Subsequent points added to this path are added to the new figure.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_StartFigure_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\startfigure.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GraphicsPath class [GDI+],StartFigure method, GraphicsPath.StartFigure, GraphicsPath::StartFigure, StartFigure, StartFigure method [GDI+], StartFigure method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_StartFigure_, gdiplus._gdiplus_CLASS_GraphicsPath_StartFigure_
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
 - GraphicsPath.StartFigure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluspath.h
: 
- GraphicsPath.StartFigure
: 
req.product: GDI+ 1.0
---

# GraphicsPath::StartFigure


## -description


The <b>GraphicsPath::StartFigure</b> method starts a new figure without closing the current figure. Subsequent points added to this path are added to the new figure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535529(v=VS.85).aspx">GraphicsPath::CloseFigure</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535458(v=VS.85).aspx">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

