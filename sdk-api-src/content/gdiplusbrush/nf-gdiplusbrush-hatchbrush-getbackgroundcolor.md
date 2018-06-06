---
UID: NF:gdiplusbrush.HatchBrush.GetBackgroundColor
title: HatchBrush::GetBackgroundColor
author: windows-sdk-content
description: The HatchBrush::GetBackgroundColor method gets the background color of this hatch brush.
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrushmethods\getbackgroundcolor.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [GDI+], GetBackgroundColor method [GDI+],HatchBrush class, HatchBrush class [GDI+],GetBackgroundColor method, HatchBrush.GetBackgroundColor, HatchBrush::GetBackgroundColor, _gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_, gdiplus._gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - HatchBrush.GetBackgroundColor
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# HatchBrush::GetBackgroundColor


## -description


The <b>HatchBrush::GetBackgroundColor</b> method gets the background color of this hatch brush.


## -parameters




### -param color [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object that receives the background color. The background color defines the color over which the hatch lines are drawn. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/7c2bfe54-3259-40d6-9eb4-1a8ad3dda477">Filling a Shape with a Hatch Pattern</a>



<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a>



<a href="https://msdn.microsoft.com/00ed2e23-ab29-488e-a509-0ba84ad05bcc">HatchBrush::GetForegroundColor</a>



<a href="https://msdn.microsoft.com/6321a75f-99cf-4e63-b498-168d4a8bb950">HatchStyle</a>
 

 

