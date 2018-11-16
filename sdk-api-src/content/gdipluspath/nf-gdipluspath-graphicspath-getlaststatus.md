---
UID: NF:gdipluspath.GraphicsPath.GetLastStatus
title: GraphicsPath::GetLastStatus
author: windows-sdk-content
description: The GraphicsPath::GetLastStatus method returns a value that indicates the nature of this GraphicsPath object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getlaststatus_91.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetLastStatus method, GraphicsPath.GetLastStatus, GraphicsPath::GetLastStatus, _gdiplus_CLASS_GraphicsPath_GetLastStatus_, gdiplus._gdiplus_CLASS_GraphicsPath_GetLastStatus_
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
 - GraphicsPath.GetLastStatus
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
- GraphicsPath.GetLastStatus
: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetLastStatus


## -description


The <b>GraphicsPath::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>GraphicsPath::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If no methods invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object have failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>GraphicsPath::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object to determine whether the constructor succeeded.

The first time you call the <b>GraphicsPath::GetLastStatus</b> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>GraphicsPath</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

