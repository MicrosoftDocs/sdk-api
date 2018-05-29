---
UID: NF:gdiplusheaders.Bitmap.UnlockBits
title: Bitmap::UnlockBits
author: windows-sdk-content
description: The Bitmap::UnlockBits method unlocks a portion of this bitmap that was previously locked by a call to Bitmap::LockBits.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\unlockbits.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Bitmap class [GDI+],UnlockBits method, Bitmap.UnlockBits, Bitmap::UnlockBits, UnlockBits, UnlockBits method [GDI+], UnlockBits method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Bitmap.UnlockBits
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Bitmap::UnlockBits


## -description


The <b>Bitmap::UnlockBits</b> method unlocks a portion of this bitmap that was previously locked by a call to <a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a>. 


## -parameters




### -param lockedBitmapData [in]

Type: <b><a href="https://msdn.microsoft.com/2682e129-5a38-474f-8713-13c3a0440a94">BitmapData</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/2682e129-5a38-474f-8713-13c3a0440a94">BitmapData</a> object that was previously passed to <a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks




<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a> and <b>Bitmap::UnlockBits</b> must be used as a pair. A call to the <b>Bitmap::LockBits</b> method of a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object establishes a temporary buffer that you can use to read or write pixel data in a specified format. After you write to the temporary buffer, a call to <b>Bitmap::UnlockBits</b> copies the pixel data in the buffer to the 
				<b>Bitmap</b> object. If the pixel format of the temporary buffer is different from the pixel format of the 
				<b>Bitmap</b> object, the pixel data is converted appropriately.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">Image Pixel Format Constants</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

