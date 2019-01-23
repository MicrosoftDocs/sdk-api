---
UID: NF:gdiplusheaders.Bitmap.Bitmap(INT,INT,INT,PixelFormat,BYTE)
title: Bitmap::Bitmap(INT,INT,INT,PixelFormat,BYTE)
author: windows-sdk-content
description: Creates a Bitmap::Bitmap object based on an array of bytes along with size and format information.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_width_height_stride_format_scan0_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_55width_height_stride_format_scan0.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(INT,INT,INT,PixelFormat,BYTE), Bitmap.Bitmap(INT,INT,INT,PixelFormat,BYTE*), Bitmap::Bitmap, Bitmap::Bitmap(INT,INT,INT,PixelFormat,BYTE), _gdiplus_CLASS_Bitmap_Bitmap_width_height_stride_format_scan0_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_width_height_stride_format_scan0_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.Bitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::Bitmap(INT,INT,INT,PixelFormat,BYTE)


## -description


Creates a <b>Bitmap::Bitmap</b> object based on an array of bytes along with size and format information.


## -parameters




### -param width [in]

Type: <b>INT</b>

Integer that specifies the width, in pixels, of the bitmap. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height, in pixels, of the bitmap. 


### -param stride [in]

Type: <b>INT</b>

Integer that specifies the byte offset between the beginning of one scan line and the next. This is usually (but not necessarily) the number of bytes in the pixel format (for example, 2 for 16 bits per pixel) multiplied by the width of the bitmap. The value passed to this parameter must be a multiple of four. 


### -param format [in]

Type: <b>PixelFormat</b>

Integer that specifies the pixel format of the bitmap. The 
					<b>PixelFormat</b> data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h. For more information about pixel format constants, see <a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>. 


### -param scan0 [in]

Type: <b>BYTE*</b>

Pointer to an array of bytes that contains the pixel data. The caller is responsible for allocating and freeing the block of memory pointed to by this parameter. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

