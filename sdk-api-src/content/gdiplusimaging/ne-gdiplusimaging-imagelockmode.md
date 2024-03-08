---
UID: NE:gdiplusimaging.ImageLockMode
title: ImageLockMode (gdiplusimaging.h)
description: The ImageLockMode enumeration specifies flags that are passed to the flags parameter of the Bitmap::LockBits method. The Bitmap::LockBits method locks a portion of an image so that you can read or write the pixel data.
helpviewer_keywords: ["ImageLockMode","ImageLockMode enumeration [GDI+]","ImageLockModeRead","ImageLockModeUserInputBuf","ImageLockModeWrite","_gdiplus_ENUM_ImageLockMode","gdiplus._gdiplus_ENUM_ImageLockMode","gdiplusimaging/ImageLockMode","gdiplusimaging/ImageLockModeRead","gdiplusimaging/ImageLockModeUserInputBuf","gdiplusimaging/ImageLockModeWrite"]
old-location: gdiplus\_gdiplus_ENUM_ImageLockMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imagelockmode.htm
ms.date: 12/05/2018
ms.keywords: ImageLockMode, ImageLockMode enumeration [GDI+], ImageLockModeRead, ImageLockModeUserInputBuf, ImageLockModeWrite, _gdiplus_ENUM_ImageLockMode, gdiplus._gdiplus_ENUM_ImageLockMode, gdiplusimaging/ImageLockMode, gdiplusimaging/ImageLockModeRead, gdiplusimaging/ImageLockModeUserInputBuf, gdiplusimaging/ImageLockModeWrite
req.header: gdiplusimaging.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ImageLockMode
 - gdiplusimaging/ImageLockMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageLockMode
---

# ImageLockMode enumeration


## -description

The <b>ImageLockMode</b> enumeration specifies flags that are passed to the 
			<i>flags</i> parameter of the 
			<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a> method. The <b>Bitmap::LockBits</b> method locks a portion of an image so that you can read or write the pixel data.

## -enum-fields

### -field ImageLockModeRead:0x0001

Specifies that a portion of the image is locked for reading.

### -field ImageLockModeWrite:0x0002

Specifies that a portion of the image is locked for writing.

### -field ImageLockModeUserInputBuf:0x0004

Specifies that the buffer used for reading or writing pixel data is allocated by the user. If this flag is set, then the 
				<i>lockedBitmapData</i> parameter of the 
				<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a> method serves as an input parameter (and possibly as an output parameter). If this flag is cleared, then the 
				<i>lockedBitmapData</i> parameter serves only as an output parameter.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-lockbits">Bitmap::LockBits</a>
