---
UID: NE:gdiplusimaging.ImageLockMode
title: ImageLockMode
author: windows-sdk-content
description: The ImageLockMode enumeration specifies flags that are passed to the flags parameter of the Bitmap::LockBits method. The Bitmap::LockBits method locks a portion of an image so that you can read or write the pixel data.
old-location: gdiplus\_gdiplus_ENUM_ImageLockMode.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imagelockmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ImageLockMode, ImageLockMode enumeration [GDI+], ImageLockModeRead, ImageLockModeUserInputBuf, ImageLockModeWrite, _gdiplus_ENUM_ImageLockMode, gdiplus._gdiplus_ENUM_ImageLockMode, gdiplusimaging/ImageLockMode, gdiplusimaging/ImageLockModeRead, gdiplusimaging/ImageLockModeUserInputBuf, gdiplusimaging/ImageLockModeWrite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdiplusimaging.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageLockMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# ImageLockMode enumeration


## -description


The <b>ImageLockMode</b> enumeration specifies flags that are passed to the 
			<i>flags</i> parameter of the 
			<a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a> method. The <b>Bitmap::LockBits</b> method locks a portion of an image so that you can read or write the pixel data.


## -enum-fields




### -field ImageLockModeRead

Specifies that a portion of the image is locked for reading. 


### -field ImageLockModeWrite

Specifies that a portion of the image is locked for writing. 


### -field ImageLockModeUserInputBuf

Specifies that the buffer used for reading or writing pixel data is allocated by the user. If this flag is set, then the 
				<i>lockedBitmapData</i> parameter of the 
				<a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a> method serves as an input parameter (and possibly as an output parameter). If this flag is cleared, then the 
				<i>lockedBitmapData</i> parameter serves only as an output parameter. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536298(v=VS.85).aspx">Bitmap::LockBits</a>
 

 

