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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/8f828820-7dd6-4dd0-959c-4dcfb1ca6ac7">GraphicsPath::CloseFigure</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/91137029-182d-4dc5-89a3-f3835f55d327">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

