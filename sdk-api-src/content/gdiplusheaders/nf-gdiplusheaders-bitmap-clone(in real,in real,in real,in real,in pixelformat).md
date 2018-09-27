---
UID: NF:gdiplusheaders.Bitmap.Clone(IN REAL,IN REAL,IN REAL,IN REAL,IN PixelFormat)
title: Bitmap::Clone(IN REAL,IN REAL,IN REAL,IN REAL,IN PixelFormat)
author: windows-sdk-content
description: The Bitmap::Clone method creates a new Bitmapobject by copying a portion of this bitmap.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Clone_REAL_x_REAL_y_REAL_width_REAL_height_PixelFormat_format_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\bitmapclonemethods\clone_82realx_realy_realwidth_realheight_pixel.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Bitmap class [GDI+],Clone method, Bitmap.Clone, Bitmap.Clone(IN REAL,IN REAL,IN REAL,IN REAL,IN PixelFormat), Bitmap.Clone(REAL,REAL,REAL,REAL,PixelFormat), Bitmap::Clone, Bitmap::Clone(IN REAL,IN REAL,IN REAL,IN REAL,IN PixelFormat), Clone, Clone method [GDI+], Clone method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_Clone_REAL_x_REAL_y_REAL_width_REAL_height_PixelFormat_format_, gdiplus._gdiplus_CLASS_Bitmap_Clone_REAL_x_REAL_y_REAL_width_REAL_height_PixelFormat_format_
ms.prod: windows-hardware
ms.technology: windows-devices
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

# Bitmap::Clone(IN REAL,IN REAL,IN REAL,IN REAL,IN PixelFormat)


## -description


The <b>Bitmap::Clone</b> method creates a new 
			<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>object by copying a portion of this bitmap.


## -parameters




### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that specifies the portion of this bitmap to copy. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that specifies the portion of this bitmap to copy. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that specifies the portion of this bitmap to copy. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that specifies the portion of this image to copy. 


### -param format [in]

Type: <b>PixelFormat</b>

Integer that specifies the pixel format of the new bitmap. The 
					<b>PixelFormat</b> data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h. For more information about pixel format constants, see <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Image Pixel Format Constants</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/f2cd46c1-914c-4b9e-a2e5-d31dceaa4826">Clone</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

