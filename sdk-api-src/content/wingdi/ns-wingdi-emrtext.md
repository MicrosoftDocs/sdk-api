---
UID: NS:wingdi.tagEMRTEXT
title: EMRTEXT (wingdi.h)
description: The EMRTEXT structure contains members for text output.
helpviewer_keywords: ["*PEMRTEXT","EMRTEXT","EMRTEXT structure [Windows GDI]","PEMRTEXT","PEMRTEXT structure pointer [Windows GDI]","_win32_EMRTEXT_str","gdi.emrtext","wingdi/EMRTEXT","wingdi/PEMRTEXT"]
old-location: gdi\emrtext.htm
tech.root: gdi
ms.assetid: a126f1ea-35ef-492d-8184-fb288a74f7f6
ms.date: 12/05/2018
ms.keywords: '*PEMRTEXT, EMRTEXT, EMRTEXT structure [Windows GDI], PEMRTEXT, PEMRTEXT structure pointer [Windows GDI], _win32_EMRTEXT_str, gdi.emrtext, wingdi/EMRTEXT, wingdi/PEMRTEXT'
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
req.typenames: EMRTEXT, *PEMRTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRTEXT
 - wingdi/tagEMRTEXT
 - PEMRTEXT
 - wingdi/PEMRTEXT
 - EMRTEXT
 - wingdi/EMRTEXT
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
 - EMRTEXT
---

# EMRTEXT structure


## -description

The <b>EMRTEXT</b> structure contains members for text output.

## -struct-fields

### -field ptlReference

The logical coordinates of the reference point used to position the string.

### -field nChars

The number of characters in the string.

### -field offString

The offset to the string.

### -field fOptions

A value that indicates how to use the application-defined rectangle. This member can be a combination of the ETO_CLIPPED and ETO_OPAQUE values.

### -field rcl

An optional clipping and/or opaquing rectangle, in logical units.

### -field offDx

The offset to the intercharacter spacing array.

## -remarks

The <b>EMRTEXT</b> structure is used as a member in the <a href="/windows/desktop/api/wingdi/ns-wingdi-emrexttextouta">EMREXTTEXTOUT</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolytextouta">EMRPOLYTEXTOUT</a> structures.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a>



<a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>