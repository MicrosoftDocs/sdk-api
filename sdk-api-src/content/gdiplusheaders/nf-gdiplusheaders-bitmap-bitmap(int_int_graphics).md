---
UID: NF:gdiplusheaders.Bitmap.Bitmap(INT,INT,Graphics)
title: Bitmap::Bitmap(IN INT,IN INT,IN Graphics) (gdiplusheaders.h)
description: Creates a Bitmap::Bitmap object based on a Graphics object, a width, and a height.
helpviewer_keywords: ["Bitmap","Bitmap class [GDI+]","Bitmap constructor","Bitmap constructor [GDI+]","Bitmap constructor [GDI+]","Bitmap class","Bitmap.Bitmap","Bitmap.Bitmap(IN INT","IN INT","IN Graphics)","Bitmap.Bitmap(INT","INT","Graphics*)","Bitmap::Bitmap","Bitmap::Bitmap(IN INT","IN INT","IN Graphics)","_gdiplus_CLASS_Bitmap_Bitmap_width_height_target_","gdiplus._gdiplus_CLASS_Bitmap_Bitmap_width_height_target_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_width_height_target_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_21width_height_target.htm
ms.date: 12/05/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(IN INT,IN INT,IN Graphics), Bitmap.Bitmap(INT,INT,Graphics*), Bitmap::Bitmap, Bitmap::Bitmap(IN INT,IN INT,IN Graphics), _gdiplus_CLASS_Bitmap_Bitmap_width_height_target_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_width_height_target_
req.header: gdiplusheaders.h
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
 - Bitmap::Bitmap
 - gdiplusheaders/Bitmap::Bitmap
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
 - Bitmap.Bitmap
---

# Bitmap::Bitmap(IN INT,IN INT,IN Graphics)


## -description

Creates a <b>Bitmap::Bitmap</b> object based on a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, a width, and a height.

## -parameters

### -param width [in]

Type: <b>INT</b>

Integer that specifies the width, in pixels, of the bitmap.

### -param height [in]

Type: <b>INT</b>

Integer that specifies the height, in pixels, of the bitmap.

### -param target [in]

Type: <b><a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains information used to initialize certain properties (for example, dots per inch) of the new <b>Bitmap::Bitmap</b> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>