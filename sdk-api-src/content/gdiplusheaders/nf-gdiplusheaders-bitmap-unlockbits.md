---
UID: NF:gdiplusheaders.Bitmap.UnlockBits
title: Bitmap::UnlockBits (gdiplusheaders.h)
description: The Bitmap::UnlockBits method unlocks a portion of this bitmap that was previously locked by a call to Bitmap::LockBits.
helpviewer_keywords: ["Bitmap class [GDI+]","UnlockBits method","Bitmap.UnlockBits","Bitmap::UnlockBits","UnlockBits","UnlockBits method [GDI+]","UnlockBits method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_","gdiplus._gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\unlockbits.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],UnlockBits method, Bitmap.UnlockBits, Bitmap::UnlockBits, UnlockBits, UnlockBits method [GDI+], UnlockBits method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_UnlockBits_lockedBitmapData_
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
 - Bitmap::UnlockBits
 - gdiplusheaders/Bitmap::UnlockBits
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
 - Bitmap.UnlockBits
---

# Bitmap::UnlockBits


## -description

The <b>Bitmap::UnlockBits</b> method unlocks a portion of this bitmap that was previously locked by a call to <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a>.

## -parameters

### -param lockedBitmapData [in]

Type: <b><a href="/previous-versions/ms534421(v=vs.85)">BitmapData</a>*</b>

Pointer to a 
					<a href="/previous-versions/ms534421(v=vs.85)">BitmapData</a> object that was previously passed to <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a> and <b>Bitmap::UnlockBits</b> must be used as a pair. A call to the <b>Bitmap::LockBits</b> method of a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object establishes a temporary buffer that you can use to read or write pixel data in a specified format. After you write to the temporary buffer, a call to <b>Bitmap::UnlockBits</b> copies the pixel data in the buffer to the 
				<b>Bitmap</b> object. If the pixel format of the temporary buffer is different from the pixel format of the 
				<b>Bitmap</b> object, the pixel data is converted appropriately.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">Image Pixel Format Constants</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>