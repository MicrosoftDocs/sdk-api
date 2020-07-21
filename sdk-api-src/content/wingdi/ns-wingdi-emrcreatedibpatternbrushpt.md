---
UID: NS:wingdi.tagEMRCREATEDIBPATTERNBRUSHPT
title: EMRCREATEDIBPATTERNBRUSHPT (wingdi.h)
description: The EMRCREATEDIBPATTERNBRUSHPT structure contains members for the CreateDIBPatternBrushPt enhanced metafile record. The BITMAPINFO structure is followed by the bitmap bits that form a packed device-independent bitmap (DIB).
helpviewer_keywords: ["*PEMRCREATEDIBPATTERNBRUSHPT","*PEMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI]","EMRCREATEDIBPATTERNBRUSHPT","EMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI]","_win32_EMRCREATEDIBPATTERNBRUSHPT_str","gdi.emrcreatedibpatternbrushpt","wingdi/*PEMRCREATEDIBPATTERNBRUSHPT","wingdi/EMRCREATEDIBPATTERNBRUSHPT"]
old-location: gdi\emrcreatedibpatternbrushpt.htm
tech.root: gdi
ms.assetid: e1d8302b-9dbe-4a92-9143-7ad03e334ee5
ms.date: 12/05/2018
ms.keywords: '*PEMRCREATEDIBPATTERNBRUSHPT, *PEMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI], EMRCREATEDIBPATTERNBRUSHPT, EMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI], _win32_EMRCREATEDIBPATTERNBRUSHPT_str, gdi.emrcreatedibpatternbrushpt, wingdi/*PEMRCREATEDIBPATTERNBRUSHPT, wingdi/EMRCREATEDIBPATTERNBRUSHPT'
f1_keywords:
- wingdi/EMRCREATEDIBPATTERNBRUSHPT
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
- EMRCREATEDIBPATTERNBRUSHPT
targetos: Windows
req.typenames: EMRCREATEDIBPATTERNBRUSHPT, *PEMRCREATEDIBPATTERNBRUSHPT
req.redist: 
ms.custom: 19H1
---

# EMRCREATEDIBPATTERNBRUSHPT structure


## -description



The <b>EMRCREATEDIBPATTERNBRUSHPT</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a> enhanced metafile record. The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure is followed by the bitmap bits that form a packed device-independent bitmap (DIB).




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihBrush

Index of brush in handle table.


### -field iUsage

Value specifying whether the <b>bmiColors</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or indices. The <b>iUsage</b> member must be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.


### -field offBmi

Offset to <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.


### -field cbBmi

Size of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.


### -field offBits

Offset to bitmap bits.


### -field cbBits

Size of bitmap bits.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

