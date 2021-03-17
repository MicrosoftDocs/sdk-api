---
UID: NS:winddi._FD_KERNINGPAIR
title: FD_KERNINGPAIR (winddi.h)
description: The FD_KERNINGPAIR structure is used to store information about kerning pairs.
helpviewer_keywords: ["FD_KERNINGPAIR","FD_KERNINGPAIR structure [Display Devices]","display.fd_kerningpair","grstrcts_5e6126d0-b3c2-4964-ab7a-f3ec90162b7e.xml","winddi/FD_KERNINGPAIR"]
old-location: display\fd_kerningpair.htm
tech.root: display
ms.assetid: 5c5eced6-a0a3-448e-bcb3-57be1b703797
ms.date: 12/05/2018
ms.keywords: FD_KERNINGPAIR, FD_KERNINGPAIR structure [Display Devices], display.fd_kerningpair, grstrcts_5e6126d0-b3c2-4964-ab7a-f3ec90162b7e.xml, winddi/FD_KERNINGPAIR
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FD_KERNINGPAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FD_KERNINGPAIR
 - winddi/_FD_KERNINGPAIR
 - FD_KERNINGPAIR
 - winddi/FD_KERNINGPAIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FD_KERNINGPAIR
---

# FD_KERNINGPAIR structure


## -description

The FD_KERNINGPAIR structure is used to store information about kerning pairs.

## -struct-fields

### -field wcFirst

Specifies the code point of the first character in the kerning pair.

### -field wcSecond

Specifies the code point of the second character in the kerning pair.

### -field fwdKern

Specifies the kerning value, in font (notional) units, for the kerning pair. If this value is greater than zero, the characters will be moved apart; otherwise, the characters will be moved together. For information about the FWORD data type, see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>.

## -remarks

An array of FD_KERNINGPAIR structures must be null-terminated, which means the last FD_KERNINGPAIR structure in the array has all structure members set to zero. An array of FD_KERNINGPAIR structures must be sorted in increasing order according to an unsigned 32-bit key, calculated as follows:


```
    wcFirst + 65536 * wcSecond.
```

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfonttree">DrvQueryFontTree</a>