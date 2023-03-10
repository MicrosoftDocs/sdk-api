---
UID: NS:wingdi._MAT2
title: MAT2 (wingdi.h)
description: The MAT2 structure contains the values for a transformation matrix used by the GetGlyphOutline function.
helpviewer_keywords: ["*LPMAT2","LPMAT2","LPMAT2 structure pointer [Windows GDI]","MAT2","MAT2 structure [Windows GDI]","_win32_MAT2_str","gdi.mat2","wingdi/LPMAT2","wingdi/MAT2"]
old-location: gdi\mat2.htm
tech.root: gdi
ms.assetid: 841883d6-bc4d-46ef-abf4-f179771d255b
ms.date: 12/05/2018
ms.keywords: '*LPMAT2, LPMAT2, LPMAT2 structure pointer [Windows GDI], MAT2, MAT2 structure [Windows GDI], _win32_MAT2_str, gdi.mat2, wingdi/LPMAT2, wingdi/MAT2'
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
req.typenames: MAT2, *LPMAT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAT2
 - wingdi/_MAT2
 - LPMAT2
 - wingdi/LPMAT2
 - MAT2
 - wingdi/MAT2
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
 - MAT2
---

# MAT2 structure


## -description

The <b>MAT2</b> structure contains the values for a transformation matrix used by the <a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphoutlinea">GetGlyphOutline</a> function.

## -struct-fields

### -field eM11

A fixed-point value for the M11 component of a 3 by 3 transformation matrix.

### -field eM12

A fixed-point value for the M12 component of a 3 by 3 transformation matrix.

### -field eM21

A fixed-point value for the M21 component of a 3 by 3 transformation matrix.

### -field eM22

A fixed-point value for the M22 component of a 3 by 3 transformation matrix.

## -remarks

The identity matrix produces a transformation in which the transformed graphical object is identical to the source object. In the identity matrix, the value of <b>eM11</b> is 1, the value of <b>eM12</b> is zero, the value of <b>eM21</b> is zero, and the value of <b>eM22</b> is 1.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphoutlinea">GetGlyphOutline</a>