---
UID: NF:gdipluspen.Pen.SetBrush
title: Pen::SetBrush (gdipluspen.h)
description: The Pen::SetBrush method sets the Brush object that a pen uses to fill a line.
helpviewer_keywords: ["Pen class [GDI+]","SetBrush method","Pen.SetBrush","Pen::SetBrush","SetBrush","SetBrush method [GDI+]","SetBrush method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetBrush_brush_","gdiplus._gdiplus_CLASS_Pen_SetBrush_brush_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetBrush_brush_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setbrush.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetBrush method, Pen.SetBrush, Pen::SetBrush, SetBrush, SetBrush method [GDI+], SetBrush method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetBrush_brush_, gdiplus._gdiplus_CLASS_Pen_SetBrush_brush_
req.header: gdipluspen.h
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Pen::SetBrush
 - gdipluspen/Pen::SetBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetBrush
---

# Pen::SetBrush


## -description

The <b>Pen::SetBrush</b> method sets the <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that a pen uses to fill a line.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object for the pen to use to fill a line.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>