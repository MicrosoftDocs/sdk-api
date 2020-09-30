---
UID: NS:wingdi._FIXED
title: FIXED (wingdi.h)
description: The FIXED structure contains the integral and fractional parts of a fixed-point real number.
helpviewer_keywords: ["FIXED","FIXED structure [Windows GDI]","_win32_FIXED_str","gdi.fixed","wingdi/FIXED"]
old-location: gdi\fixed.htm
tech.root: gdi
ms.assetid: b1d94060-e822-447f-82ba-fd1cf2ddaa3b
ms.date: 12/05/2018
ms.keywords: FIXED, FIXED structure [Windows GDI], _win32_FIXED_str, gdi.fixed, wingdi/FIXED
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
req.typenames: FIXED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FIXED
 - wingdi/_FIXED
 - FIXED
 - wingdi/FIXED
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
 - FIXED
---

# FIXED structure


## -description

The <b>FIXED</b> structure contains the integral and fractional parts of a fixed-point real number.

## -struct-fields

### -field value

The integer part of the number.

### -field fract

The fractional part of the number.

## -remarks

The <b>FIXED</b> structure is used to describe the elements of the <a href="/windows/desktop/api/wingdi/ns-wingdi-mat2">MAT2</a> structure.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-mat2">MAT2</a>