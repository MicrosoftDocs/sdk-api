---
UID: NF:gdiplusbrush.HatchBrush.GetForegroundColor
title: HatchBrush::GetForegroundColor
author: windows-sdk-content
description: The HatchBrush::GetForegroundColor method gets the foreground color of this hatch brush.
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_GetForegroundColor_color_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrushmethods\getforegroundcolor.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetForegroundColor, GetForegroundColor method [GDI+], GetForegroundColor method [GDI+],HatchBrush class, HatchBrush class [GDI+],GetForegroundColor method, HatchBrush.GetForegroundColor, HatchBrush::GetForegroundColor, _gdiplus_CLASS_HatchBrush_GetForegroundColor_color_, gdiplus._gdiplus_CLASS_HatchBrush_GetForegroundColor_color_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusbrush.h
req.include-header: Gdiplus.h
req.redist: 
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
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - HatchBrush.GetForegroundColor
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# HatchBrush::GetForegroundColor


## -description


The <b>HatchBrush::GetForegroundColor</b> method gets the foreground color of this hatch brush.


## -parameters




### -param color [out]

Type: <b><a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that receives the foreground color. The foreground color defines the color of the hatch lines. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533857(v=VS.85).aspx">Filling a Shape with a Hatch Pattern</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534127(v=VS.85).aspx">HatchStyle</a>
 

 

