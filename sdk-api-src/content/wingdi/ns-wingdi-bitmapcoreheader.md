---
UID: NS:wingdi.tagBITMAPCOREHEADER
title: BITMAPCOREHEADER (wingdi.h)
description: The BITMAPCOREHEADER structure contains information about the dimensions and color format of a DIB.
helpviewer_keywords: ["*LPBITMAPCOREHEADER","*PBITMAPCOREHEADER","BITMAPCOREHEADER","BITMAPCOREHEADER structure [Windows GDI]","PBITMAPCOREHEADER","PBITMAPCOREHEADER structure pointer [Windows GDI]","_win32_BITMAPCOREHEADER_str","gdi.bitmapcoreheader","wingdi/BITMAPCOREHEADER","wingdi/PBITMAPCOREHEADER"]
old-location: gdi\bitmapcoreheader.htm
tech.root: gdi
ms.assetid: 0182adcd-dbba-43de-b41b-ab2f0fd8f7bf
ms.date: 12/05/2018
ms.keywords: '*LPBITMAPCOREHEADER, *PBITMAPCOREHEADER, BITMAPCOREHEADER, BITMAPCOREHEADER structure [Windows GDI], PBITMAPCOREHEADER, PBITMAPCOREHEADER structure pointer [Windows GDI], _win32_BITMAPCOREHEADER_str, gdi.bitmapcoreheader, wingdi/BITMAPCOREHEADER, wingdi/PBITMAPCOREHEADER'
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
targetos: Windows
req.typenames: BITMAPCOREHEADER, *LPBITMAPCOREHEADER, *PBITMAPCOREHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBITMAPCOREHEADER
 - wingdi/tagBITMAPCOREHEADER
 - LPBITMAPCOREHEADER
 - wingdi/LPBITMAPCOREHEADER
 - BITMAPCOREHEADER
 - wingdi/BITMAPCOREHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAPCOREHEADER
---

# BITMAPCOREHEADER structure


## -description

The <b>BITMAPCOREHEADER</b> structure contains information about the dimensions and color format of a DIB.

## -struct-fields

### -field bcSize

The number of bytes required by the structure.

### -field bcWidth

The width of the bitmap, in pixels.

### -field bcHeight

The height of the bitmap, in pixels.

### -field bcPlanes

The number of planes for the target device. This value must be 1.

### -field bcBitCount

The number of bits-per-pixel. This value must be 1, 4, 8, or 24.

## -remarks

The <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a> structure combines the <b>BITMAPCOREHEADER</b> structure and a color table to provide a complete definition of the dimensions and colors of a DIB. For more information about specifying a DIB, see <b>BITMAPCOREINFO</b>.

An application should use the information stored in the <b>bcSize</b> member to locate the color table in a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a> structure, using a method such as the following:


```cpp

pColor = ((LPBYTE) pBitmapCoreInfo + 
        (WORD) (pBitmapCoreInfo -> bcSize)) 

```

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>