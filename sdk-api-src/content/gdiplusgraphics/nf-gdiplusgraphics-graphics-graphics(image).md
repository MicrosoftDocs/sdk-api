---
UID: NF:gdiplusgraphics.Graphics.Graphics(Image)
title: Graphics::Graphics(IN Image) (gdiplusgraphics.h)
description: Creates a Graphics::Graphics object that is associated with an Image object.
helpviewer_keywords: ["Graphics","Graphics class [GDI+]","Graphics constructor","Graphics constructor [GDI+]","Graphics constructor [GDI+]","Graphics class","Graphics.Graphics","Graphics.Graphics(IN Image)","Graphics.Graphics(Image*)","Graphics::Graphics","Graphics::Graphics(IN Image)","_gdiplus_CLASS_Graphics_Graphics_image_","gdiplus._gdiplus_CLASS_Graphics_Graphics_image_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Graphics_image_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsconstructors\graphics_30image.htm
ms.date: 12/05/2018
ms.keywords: Graphics, Graphics class [GDI+],Graphics constructor, Graphics constructor [GDI+], Graphics constructor [GDI+],Graphics class, Graphics.Graphics, Graphics.Graphics(IN Image), Graphics.Graphics(Image*), Graphics::Graphics, Graphics::Graphics(IN Image), _gdiplus_CLASS_Graphics_Graphics_image_, gdiplus._gdiplus_CLASS_Graphics_Graphics_image_
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

# Graphics::Graphics(IN Image)


## -description

Creates a <b>Graphics::Graphics</b> object that is associated with an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param image [in]

Type: <b>Image*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that will be associated with the new <b>Graphics::Graphics</b> object.

## -remarks

This constructor fails if the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object is based on a metafile that was opened for reading. The 
				<b>Image::Image(file)</b> and 
				<b>Metafile::Metafile(file)</b> constructors open a metafile for reading. To open a metafile for recording, use a 
				<b>Metafile</b> constructor that receives a device context handle.

This constructor also fails if the image uses one of the following pixel formats: 

<ul>
<li>PixelFormatUndefined </li>
<li>PixelFormatDontCare </li>
<li>PixelFormat1bppIndexed </li>
<li>PixelFormat4bppIndexed </li>
<li>PixelFormat8bppIndexed </li>
<li>PixelFormat16bppGrayScale </li>
<li>PixelFormat16bppARGB1555 </li>
</ul>

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/gdiplus/-gdiplus-getting-started-use">Getting Started</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-graphics(constgraphics_)">Graphics Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>