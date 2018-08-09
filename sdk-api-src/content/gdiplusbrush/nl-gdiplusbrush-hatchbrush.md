---
UID: NL:gdiplusbrush.HatchBrush
title: HatchBrush
author: windows-sdk-content
description: This HatchBrush class defines a rectangular brush with a hatch style, a foreground color, and a background color.
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrush.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: HatchBrush, HatchBrush class [GDI+], HatchBrush class [GDI+],described, _gdiplus_CLASS_HatchBrush_Class, gdiplus._gdiplus_CLASS_HatchBrush_Class, gdiplusbrush/HatchBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdiplusbrush.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - gdiplusbrush.h
api_name:
 - HatchBrush
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# HatchBrush class


## -description


This <a href="https://msdn.microsoft.com/f1c7c756-12c3-469d-9fe1-03b01f8ac269">HatchBrush</a> class defines a rectangular brush with a hatch style, a foreground color, and a background color. There are six hatch styles. The foreground color defines the color of the hatch lines; the background color defines the color over which the hatch lines are drawn.


## -remarks



Hatches are applied to shape interiors in the device space. As a result, they maintain their appearance in device space and are unaffected by current transformations in the graphics context. Such brushes are also called nonscalable brushes. Hatches are aligned at the upper-left corner of the display device. When the graphics engine uses a <a href="https://msdn.microsoft.com/f1c7c756-12c3-469d-9fe1-03b01f8ac269">HatchBrush</a> object to paint a shape, it first transforms the shape to device space before applying the hatch to the interiors. Hatches are always tiled to paint the interiors.



