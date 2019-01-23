---
UID: NF:gdiplusheaders.Bitmap.Clone(IN const RectF &,IN PixelFormat)
title: Bitmap::Clone(IN const RectF &,IN PixelFormat)
author: windows-sdk-content
description: The Bitmap::Clone method creates a new Bitmap object by copying a portion of this bitmap.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Clone_RectF_rect_PixelFormat_format_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\bitmapclonemethods\clone_1rectfamprect_pixelformatformat.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Bitmap class [GDI+],Clone method, Bitmap.Clone, Bitmap.Clone(IN const RectF &,IN PixelFormat), Bitmap.Clone(const RectF&,PixelFormat), Bitmap::Clone, Bitmap::Clone(IN const RectF &,IN PixelFormat), Clone, Clone method [GDI+], Clone method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_Clone_RectF_rect_PixelFormat_format_, gdiplus._gdiplus_CLASS_Bitmap_Clone_RectF_rect_PixelFormat_format_
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
 - Bitmap.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::Clone(IN const RectF &,IN PixelFormat)


## -description


The <b>Bitmap::Clone</b> method creates a new 
			<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object by copying a portion of this bitmap.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to a rectangle that specifies the portion of this bitmap to be copied. 


### -param format [in]

Type: <b>PixelFormat</b>

Integer that specifies the pixel format of the new bitmap. The 
					<b>PixelFormat</b> data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h. For more information about pixel format constants, see <a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536287(v=VS.85).aspx">Clone</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

