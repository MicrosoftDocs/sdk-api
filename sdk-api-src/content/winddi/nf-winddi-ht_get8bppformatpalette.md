---
UID: NF:winddi.HT_Get8BPPFormatPalette
title: HT_Get8BPPFormatPalette function (winddi.h)
description: The HT_Get8BPPFormatPalette function returns a halftone palette for use on standard 8-bits per pixel device types.
helpviewer_keywords: ["HT_Get8BPPFormatPalette","HT_Get8BPPFormatPalette function [Display Devices]","display.ht_get8bppformatpalette","gdifncs_78b4c867-b035-4cc3-9386-2922df0e9c12.xml","winddi/HT_Get8BPPFormatPalette"]
old-location: display\ht_get8bppformatpalette.htm
tech.root: display
ms.assetid: 0f6d81b8-2ad2-4bcc-a5cc-5b2f396aaa75
ms.date: 12/05/2018
ms.keywords: HT_Get8BPPFormatPalette, HT_Get8BPPFormatPalette function [Display Devices], display.ht_get8bppformatpalette, gdifncs_78b4c867-b035-4cc3-9386-2922df0e9c12.xml, winddi/HT_Get8BPPFormatPalette
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HT_Get8BPPFormatPalette
 - winddi/HT_Get8BPPFormatPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - HT_Get8BPPFormatPalette
---

# HT_Get8BPPFormatPalette function


## -description

The <b>HT_Get8BPPFormatPalette</b> function returns a halftone palette for use on standard 8-bits per pixel device types.

## -parameters

### -param pPaletteEntry [out]

Pointer to an array of PALETTEENTRY structures (described in the Microsoft Windows SDK documentation). When this pointer is not <b>NULL</b>, GDI assumes that it points to valid memory space in which GDI can place the entire 8-bits per pixel halftone palette.

### -param RedGamma [in]

Specifies the red, green, and blue gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param GreenGamma [in]

Specifies the red, green, and blue gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

### -param BlueGamma [in]

Specifies the red, green, and blue gamma value. This USHORT value is interpreted as a real number whose four least-significant digits are to the right of the (implied) decimal point. For example, a gamma value of 10000 represents the real number 1.0000, and 12345 represents 1.2345. The minimum gamma value allowed is 0.0000, and the maximum allowable value is 6.5535.

## -returns

If <i>pPaletteEntry</i> is not <b>NULL</b>, the return value is the number of PALETTEENTRY structures that GDI filled in starting at the memory location pointed to by <i>pPaletteEntry</i>. If <i>pPaletteEntry</i> is <b>NULL</b>, the return value is the total count of PALETTEENTRY structures required to store the 8-bits per pixel halftone palette.

## -remarks

<b>HT_Get8BPPFormatPalette</b> is a halftone-related GDI service that drivers can use to acquire the system's standard 8-bits per pixel halftone palette.

