---
UID: NF:gdiplusheaders.Bitmap.LockBits
title: Bitmap::LockBits
author: windows-sdk-content
description: The Bitmap::LockBits method locks a rectangular portion of this bitmap and provides a temporary buffer that you can use to read or write pixel data in a specified format.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_LockBits_rect_flags_format_lockedBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\lockbits.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Bitmap class [GDI+],LockBits method, Bitmap.LockBits, Bitmap::LockBits, LockBits, LockBits method [GDI+], LockBits method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_LockBits_rect_flags_format_lockedBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_LockBits_rect_flags_format_lockedBitmapData_
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
 - Bitmap.LockBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::LockBits


## -description


The <b>Bitmap::LockBits</b> method locks a rectangular portion of this bitmap and provides a temporary buffer that you can use to read or write pixel data in a specified format. Any pixel data that you write to the buffer is copied to the 
			<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object when you call <a href="https://msdn.microsoft.com/45d92c06-8d86-40ca-b721-efe092a4aea9">Bitmap::UnlockBits</a>.


## -parameters




### -param rect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to a rectangle that specifies the portion of the bitmap to be locked. 


### -param flags [in]

Type: <b>UINT</b>

Set of flags that specify whether the locked portion of the bitmap is available for reading or for writing and whether the caller has already allocated a buffer. Individual flags are defined in the <a href="https://msdn.microsoft.com/2beb5437-9d26-4642-aff8-20faa87be199">ImageLockMode</a> enumeration. 


### -param format [in]

Type: <b>PixelFormat</b>

Integer that specifies the format of the pixel data in the temporary buffer. The pixel format of the temporary buffer does not have to be the same as the pixel format of this 
					<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object. The 
					<b>PixelFormat</b> data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h. For more information about pixel format constants, see <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Image Pixel Format Constants</a>. GDI+ version 1.0 does not support processing of 16-bits-per-channel images, so you should not set this parameter equal to PixelFormat48bppRGB, PixelFormat64bppARGB, or PixelFormat64bppPARGB. 


### -param lockedBitmapData [in, out]

Type: <b><a href="https://msdn.microsoft.com/2682e129-5a38-474f-8713-13c3a0440a94">BitmapData</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2682e129-5a38-474f-8713-13c3a0440a94">BitmapData</a> object. If the ImageLockModeUserInputBuf flag of the 
					<i>flags</i> parameter is cleared, then 
					<i>lockedBitmapData</i> serves only as an output parameter. In that case, the 
					<b>Scan0</b> data member of the <b>BitmapData</b> object receives a pointer to a temporary buffer, which is filled with the values of the requested pixels. The other data members of the <b>BitmapData</b> object receive attributes (width, height, format, and stride) of the pixel data in the temporary buffer. If the pixel data is stored bottom-up, the 
					<b>Stride</b> data member is negative. If the pixel data is stored top-down, the 
					<b>Stride</b> data member is positive. If the ImageLockModeUserInputBuf flag of the 
					<i>flags</i> parameter is set, then 
					<i>lockedBitmapData</i> serves as an input parameter (and possibly as an output parameter). In that case, the caller must allocate a buffer for the pixel data that will be read or written. The caller also must create a <b>BitmapData</b> object, set the 
					<b>Scan0</b> data member of that <b>BitmapData</b> object to the address of the buffer, and set the other data members of the <b>BitmapData</b> object to specify the attributes (width, height, format, and stride) of the buffer. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/45d92c06-8d86-40ca-b721-efe092a4aea9">Bitmap::UnlockBits</a>



<a href="https://msdn.microsoft.com/2682e129-5a38-474f-8713-13c3a0440a94">BitmapData</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/2beb5437-9d26-4642-aff8-20faa87be199">ImageLockMode</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

