---
UID: NS:wingdi.tagBITMAPFILEHEADER
title: BITMAPFILEHEADER (wingdi.h)
description: The BITMAPFILEHEADER structure contains information about the type, size, and layout of a file that contains a DIB.
old-location: gdi\bitmapfileheader.htm
tech.root: gdi
ms.assetid: ae24c4db-fc29-4c97-bf78-069794c8d844
ms.date: 12/05/2018
ms.keywords: '*LPBITMAPFILEHEADER, *PBITMAPFILEHEADER, BITMAPFILEHEADER, BITMAPFILEHEADER structure [Windows GDI], PBITMAPFILEHEADER, PBITMAPFILEHEADER structure pointer [Windows GDI], _win32_BITMAPFILEHEADER_str, gdi.bitmapfileheader, wingdi/BITMAPFILEHEADER, wingdi/PBITMAPFILEHEADER'
ms.topic: struct
f1_keywords:
- wingdi/BITMAPFILEHEADER
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wingdi.h
api_name:
- BITMAPFILEHEADER
targetos: Windows
req.typenames: BITMAPFILEHEADER, *LPBITMAPFILEHEADER, *PBITMAPFILEHEADER
req.redist: 
ms.custom: 19H1
---

# BITMAPFILEHEADER structure


## -description



The <b>BITMAPFILEHEADER</b> structure contains information about the type, size, and layout of a file that contains a DIB.




## -struct-fields




### -field bfType

The file type; must be BM.


### -field bfSize

The size, in bytes, of the bitmap file.


### -field bfReserved1

Reserved; must be zero.


### -field bfReserved2

Reserved; must be zero.


### -field bfOffBits

The offset, in bytes, from the beginning of the <b>BITMAPFILEHEADER</b> structure to the bitmap bits.


## -remarks



A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a> structure immediately follows the <b>BITMAPFILEHEADER</b> structure in the DIB file. For more information, see <a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-storage">Bitmap Storage</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>
 

 

