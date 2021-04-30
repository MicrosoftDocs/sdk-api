---
UID: NS:wingdi.tagRGBTRIPLE
title: RGBTRIPLE (wingdi.h)
description: The RGBTRIPLE structure describes a color consisting of relative intensities of red, green, and blue. The bmciColors member of the BITMAPCOREINFO structure consists of an array of RGBTRIPLE structures.
helpviewer_keywords: ["*LPRGBTRIPLE","*NPRGBTRIPLE","*PRGBTRIPLE","RGBTRIPLE","RGBTRIPLE structure [Windows GDI]","_win32_RGBTRIPLE_str","gdi.rgbtriple","wingdi/RGBTRIPLE"]
old-location: gdi\rgbtriple.htm
tech.root: gdi
ms.assetid: bc1467a5-0027-4f22-bfc9-1deab562c573
ms.date: 12/05/2018
ms.keywords: '*LPRGBTRIPLE, *NPRGBTRIPLE, *PRGBTRIPLE, RGBTRIPLE, RGBTRIPLE structure [Windows GDI], _win32_RGBTRIPLE_str, gdi.rgbtriple, wingdi/RGBTRIPLE'
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
req.typenames: RGBTRIPLE, *PRGBTRIPLE, *NPRGBTRIPLE, *LPRGBTRIPLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRGBTRIPLE
 - wingdi/tagRGBTRIPLE
 - PRGBTRIPLE
 - wingdi/PRGBTRIPLE
 - RGBTRIPLE
 - wingdi/RGBTRIPLE
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
 - RGBTRIPLE
---

# RGBTRIPLE structure


## -description

The <b>RGBTRIPLE</b> structure describes a color consisting of relative intensities of red, green, and blue. The <b>bmciColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a> structure consists of an array of <b>RGBTRIPLE</b> structures.

## -struct-fields

### -field rgbtBlue

The intensity of blue in the color.

### -field rgbtGreen

The intensity of green in the color.

### -field rgbtRed

The intensity of red in the color.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapcoreinfo">BITMAPCOREINFO</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>