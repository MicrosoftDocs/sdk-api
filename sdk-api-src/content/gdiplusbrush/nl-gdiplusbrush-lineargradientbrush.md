---
UID: NL:gdiplusbrush.LinearGradientBrush
title: LinearGradientBrush (gdiplusbrush.h)
description: The LinearGradientBrush class defines a brush that paints a color gradient in which the color changes evenly from the starting boundary line of the linear gradient brush to the ending boundary line of the linear gradient brush.
helpviewer_keywords: ["LinearGradientBrush","LinearGradientBrush class [GDI+]","LinearGradientBrush class [GDI+]","described","_gdiplus_CLASS_LinearGradientBrush_Class","gdiplus._gdiplus_CLASS_LinearGradientBrush_Class","gdiplusbrush/LinearGradientBrush"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrush.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+], LinearGradientBrush class [GDI+],described, _gdiplus_CLASS_LinearGradientBrush_Class, gdiplus._gdiplus_CLASS_LinearGradientBrush_Class, gdiplusbrush/LinearGradientBrush
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
 - LinearGradientBrush
 - gdiplusbrush/LinearGradientBrush
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
 - LinearGradientBrush
---

# LinearGradientBrush class


## -description

The <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-lineargradientbrush(constlineargradientbrush_)">LinearGradientBrush</a> class defines a brush that paints a color gradient in which the color changes evenly from the starting boundary line of the linear gradient brush to the ending boundary line of the linear gradient brush. The boundary lines of a linear gradient brush are two parallel straight lines. The color gradient is perpendicular to the boundary lines of the linear gradient brush, changing gradually across the stroke from the starting boundary line to the ending boundary line. The color gradient has one color at the starting boundary line and another color at the ending boundary line.