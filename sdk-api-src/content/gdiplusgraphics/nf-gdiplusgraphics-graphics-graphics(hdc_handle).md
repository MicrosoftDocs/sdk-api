---
UID: NF:gdiplusgraphics.Graphics.Graphics(HDC,HANDLE)
title: Graphics::Graphics(IN HDC,IN HANDLE) (gdiplusgraphics.h)
description: Creates a Graphics::Graphics object that is associated with a specified device context and a specified device.
helpviewer_keywords: ["Graphics","Graphics class [GDI+]","Graphics constructor","Graphics constructor [GDI+]","Graphics constructor [GDI+]","Graphics class","Graphics.Graphics","Graphics.Graphics(HDC","HANDLE)","Graphics.Graphics(IN HDC","IN HANDLE)","Graphics::Graphics","Graphics::Graphics(IN HDC","IN HANDLE)","_gdiplus_CLASS_Graphics_Graphics_hdc_hdevice_","gdiplus._gdiplus_CLASS_Graphics_Graphics_hdc_hdevice_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Graphics_hdc_hdevice_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsconstructors\graphics_73hdc_hdevice.htm
ms.date: 12/05/2018
ms.keywords: Graphics, Graphics class [GDI+],Graphics constructor, Graphics constructor [GDI+], Graphics constructor [GDI+],Graphics class, Graphics.Graphics, Graphics.Graphics(HDC,HANDLE), Graphics.Graphics(IN HDC,IN HANDLE), Graphics::Graphics, Graphics::Graphics(IN HDC,IN HANDLE), _gdiplus_CLASS_Graphics_Graphics_hdc_hdevice_, gdiplus._gdiplus_CLASS_Graphics_Graphics_hdc_hdevice_
req.header: gdiplusgraphics.h
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
 - Graphics::Graphics
 - gdiplusgraphics/Graphics::Graphics
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
 - Graphics.Graphics
---

# Graphics::Graphics(IN HDC,IN HANDLE)


## -description

Creates a <b>Graphics::Graphics</b> object that is associated with a specified device context and a specified device.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

Handle to a device context that will be associated with the new <b>Graphics::Graphics</b> object.

### -param hdevice [in]

Type: <b>HANDLE</b>

Handle to a device that will be associated with the new <b>Graphics::Graphics</b> object.

## -remarks

When you use this constructor to create a <b>Graphics::Graphics</b> object, make sure that the <b>Graphics::Graphics</b> object is deleted or goes out of scope before the device context is released.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="/windows/desktop/gdiplus/-gdiplus-optimizing-printing-by-providing-a-printer-handle-use">Optimizing Printing by Providing a Printer Handle</a>