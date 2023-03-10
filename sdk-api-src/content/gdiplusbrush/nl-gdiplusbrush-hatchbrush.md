---
UID: NL:gdiplusbrush.HatchBrush
title: HatchBrush (gdiplusbrush.h)
description: This HatchBrush class defines a rectangular brush with a hatch style, a foreground color, and a background color.
helpviewer_keywords: ["HatchBrush","HatchBrush class [GDI+]","HatchBrush class [GDI+]","described","_gdiplus_CLASS_HatchBrush_Class","gdiplus._gdiplus_CLASS_HatchBrush_Class","gdiplusbrush/HatchBrush"]
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrush.htm
ms.date: 12/05/2018
ms.keywords: HatchBrush, HatchBrush class [GDI+], HatchBrush class [GDI+],described, _gdiplus_CLASS_HatchBrush_Class, gdiplus._gdiplus_CLASS_HatchBrush_Class, gdiplusbrush/HatchBrush
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HatchBrush
 - gdiplusbrush/HatchBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusbrush.h
api_name:
 - HatchBrush
---

# HatchBrush class


## -description

This <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)">HatchBrush</a> class defines a rectangular brush with a hatch style, a foreground color, and a background color. There are six hatch styles. The foreground color defines the color of the hatch lines; the background color defines the color over which the hatch lines are drawn.

## -remarks

Hatches are applied to shape interiors in the device space. As a result, they maintain their appearance in device space and are unaffected by current transformations in the graphics context. Such brushes are also called nonscalable brushes. Hatches are aligned at the upper-left corner of the display device. When the graphics engine uses a <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)">HatchBrush</a> object to paint a shape, it first transforms the shape to device space before applying the hatch to the interiors. Hatches are always tiled to paint the interiors.