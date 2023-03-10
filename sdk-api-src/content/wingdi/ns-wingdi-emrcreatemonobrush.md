---
UID: NS:wingdi.tagEMRCREATEMONOBRUSH
title: EMRCREATEMONOBRUSH (wingdi.h)
description: The EMRCREATEMONOBRUSH structure contains members for the CreatePatternBrush (when passed a monochrome bitmap) or CreateDIBPatternBrush (when passed a monochrome DIB) enhanced metafile records.
helpviewer_keywords: ["*PEMRCREATEMONOBRUSH","EMRCREATEMONOBRUSH","EMRCREATEMONOBRUSH structure [Windows GDI]","PEMRCREATEMONOBRUSH","PEMRCREATEMONOBRUSH structure pointer [Windows GDI]","_win32_EMRCREATEMONOBRUSH_str","gdi.emrcreatemonobrush","wingdi/EMRCREATEMONOBRUSH","wingdi/PEMRCREATEMONOBRUSH"]
old-location: gdi\emrcreatemonobrush.htm
tech.root: gdi
ms.assetid: 6f581ad4-0449-40b1-bcc6-737bfcdc33c4
ms.date: 12/05/2018
ms.keywords: '*PEMRCREATEMONOBRUSH, EMRCREATEMONOBRUSH, EMRCREATEMONOBRUSH structure [Windows GDI], PEMRCREATEMONOBRUSH, PEMRCREATEMONOBRUSH structure pointer [Windows GDI], _win32_EMRCREATEMONOBRUSH_str, gdi.emrcreatemonobrush, wingdi/EMRCREATEMONOBRUSH, wingdi/PEMRCREATEMONOBRUSH'
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
req.typenames: EMRCREATEMONOBRUSH, *PEMRCREATEMONOBRUSH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRCREATEMONOBRUSH
 - wingdi/tagEMRCREATEMONOBRUSH
 - PEMRCREATEMONOBRUSH
 - wingdi/PEMRCREATEMONOBRUSH
 - EMRCREATEMONOBRUSH
 - wingdi/EMRCREATEMONOBRUSH
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
 - EMRCREATEMONOBRUSH
---

# EMRCREATEMONOBRUSH structure


## -description

The <b>EMRCREATEMONOBRUSH</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a> (when passed a monochrome bitmap) or <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a> (when passed a monochrome DIB) enhanced metafile records.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihBrush

Index of brush in handle table.

### -field iUsage

Value specifying whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or indices. The <b>iUsage</b> member must be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.

### -field offBmi

Offset to <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field cbBmi

Size of <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -field offBits

Offset to bitmap bits.

### -field cbBits

Size of bitmap bits.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>