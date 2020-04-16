---
UID: NF:gdiplusbrush.HatchBrush.GetForegroundColor
title: HatchBrush::GetForegroundColor (gdiplusbrush.h)
description: The HatchBrush::GetForegroundColor method gets the foreground color of this hatch brush.helpviewer_keywords: ["GetForegroundColor","GetForegroundColor method [GDI+]","GetForegroundColor method [GDI+]","HatchBrush class","HatchBrush class [GDI+]","GetForegroundColor method","HatchBrush.GetForegroundColor","HatchBrush::GetForegroundColor","_gdiplus_CLASS_HatchBrush_GetForegroundColor_color_","gdiplus._gdiplus_CLASS_HatchBrush_GetForegroundColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_GetForegroundColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrushmethods\getforegroundcolor.htm
ms.date: 12/05/2018
ms.keywords: GetForegroundColor, GetForegroundColor method [GDI+], GetForegroundColor method [GDI+],HatchBrush class, HatchBrush class [GDI+],GetForegroundColor method, HatchBrush.GetForegroundColor, HatchBrush::GetForegroundColor, _gdiplus_CLASS_HatchBrush_GetForegroundColor_color_, gdiplus._gdiplus_CLASS_HatchBrush_GetForegroundColor_color_
f1_keywords:
- gdiplusbrush/HatchBrush.GetForegroundColor
dev_langs:
- c++
req.header: gdiplusbrush.h
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
- HatchBrush.GetForegroundColor
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# HatchBrush::GetForegroundColor


## -description


The <b>HatchBrush::GetForegroundColor</b> method gets the foreground color of this hatch brush.


## -parameters




### -param color [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that receives the foreground color. The foreground color defines the color of the hatch lines. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-hatch-pattern-use">Filling a Shape with a Hatch Pattern</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hatchstyle">HatchStyle</a>
 

 

