---
UID: NF:gdiplusheaders.Bitmap.Clone(INT,INT,INT,INT,PixelFormat)
title: Bitmap::Clone(IN INT,IN INT,IN INT,IN INT,IN PixelFormat) (gdiplusheaders.h)
description: The Bitmap::Clone method creates a new Bitmapobject by copying a portion of this bitmap. (overload 1/2)
helpviewer_keywords: ["Bitmap class [GDI+]","Clone method","Bitmap.Clone","Bitmap.Clone(IN INT","IN INT","IN INT","IN INT","IN PixelFormat)","Bitmap.Clone(INT","INT","INT","INT","PixelFormat)","Bitmap::Clone","Bitmap::Clone(IN INT","IN INT","IN INT","IN INT","IN PixelFormat)","Clone","Clone method [GDI+]","Clone method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_Clone_INT_x_INT_y_INT_width_INT_height_PixelFormat_format_","gdiplus._gdiplus_CLASS_Bitmap_Clone_INT_x_INT_y_INT_width_INT_height_PixelFormat_format_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Clone_INT_x_INT_y_INT_width_INT_height_PixelFormat_format_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\bitmapclonemethods\clone_83intx_inty_intwidth_intheight_pixelform.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],Clone method, Bitmap.Clone, Bitmap.Clone(IN INT,IN INT,IN INT,IN INT,IN PixelFormat), Bitmap.Clone(INT,INT,INT,INT,PixelFormat), Bitmap::Clone, Bitmap::Clone(IN INT,IN INT,IN INT,IN INT,IN PixelFormat), Clone, Clone method [GDI+], Clone method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_Clone_INT_x_INT_y_INT_width_INT_height_PixelFormat_format_, gdiplus._gdiplus_CLASS_Bitmap_Clone_INT_x_INT_y_INT_width_INT_height_PixelFormat_format_
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
 - Bitmap::Clone
 - gdiplusheaders/Bitmap::Clone
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
 - Bitmap.Clone
---

# Bitmap::Clone(IN INT,IN INT,IN INT,IN INT,IN PixelFormat)


## -description

The <b>Bitmap::Clone</b> method creates a new 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object by copying a portion of this bitmap.

## -parameters

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle that specifies the portion of this bitmap to copy.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle that specifies the portion of this bitmap to copy.

### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle that specifies the portion of this bitmap to copy.

### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle that specifies the portion of this image to copy.

### -param format [in]

Type: <b>PixelFormat</b>

Integer that specifies the pixel format of the new bitmap. The 
					<b>PixelFormat</b> data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h. For more information about pixel format constants, see <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">Image Pixel Format Constants</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)">Clone</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">Image Pixel Format Constants</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
