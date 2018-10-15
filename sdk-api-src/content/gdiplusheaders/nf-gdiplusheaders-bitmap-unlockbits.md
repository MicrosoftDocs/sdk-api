---
UID: NF:gdiplusheaders.Bitmap.UnlockBits
title: Bitmap::UnlockBits
author: windows-sdk-content
description: The Bitmap::UnlockBits method unlocks a portion of this bitmap that was previously locked by a call to Bitmap::LockBits.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\unlockbits.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Bitmap class [GDI+],UnlockBits method, Bitmap.UnlockBits, Bitmap::UnlockBits, UnlockBits, UnlockBits method [GDI+], UnlockBits method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_
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
 - Bitmap.UnlockBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::UnlockBits


## -description


The <b>Bitmap::UnlockBits</b> method unlocks a portion of this bitmap that was previously locked by a call to <a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a>. 


## -parameters




### -param lockedBitmapData [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534421(v=VS.85).aspx">BitmapData</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534421(v=VS.85).aspx">BitmapData</a> object that was previously passed to <a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks




<a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a> and <b>Bitmap::UnlockBits</b> must be used as a pair. A call to the <b>Bitmap::LockBits</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object establishes a temporary buffer that you can use to read or write pixel data in a specified format. After you write to the temporary buffer, a call to <b>Bitmap::UnlockBits</b> copies the pixel data in the buffer to the 
				<b>Bitmap</b> object. If the pixel format of the temporary buffer is different from the pixel format of the 
				<b>Bitmap</b> object, the pixel data is converted appropriately.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

