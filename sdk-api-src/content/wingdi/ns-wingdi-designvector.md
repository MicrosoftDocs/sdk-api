---
UID: NS:wingdi.tagDESIGNVECTOR
title: DESIGNVECTOR (wingdi.h)
description: The DESIGNVECTOR structure is used by an application to specify values for the axes of a multiple master font.
helpviewer_keywords: ["*LPDESIGNVECTOR","*PDESIGNVECTOR","DESIGNVECTOR","DESIGNVECTOR structure [Windows GDI]","PDESIGNVECTOR","PDESIGNVECTOR structure pointer [Windows GDI]","_win32_DESIGNVECTOR_str","gdi.designvector","wingdi/DESIGNVECTOR","wingdi/PDESIGNVECTOR"]
old-location: gdi\designvector.htm
tech.root: gdi
ms.assetid: aeff9901-2405-44aa-ba46-8d784afd6b76
ms.date: 12/05/2018
ms.keywords: '*LPDESIGNVECTOR, *PDESIGNVECTOR, DESIGNVECTOR, DESIGNVECTOR structure [Windows GDI], PDESIGNVECTOR, PDESIGNVECTOR structure pointer [Windows GDI], _win32_DESIGNVECTOR_str, gdi.designvector, wingdi/DESIGNVECTOR, wingdi/PDESIGNVECTOR'
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
req.typenames: DESIGNVECTOR, *PDESIGNVECTOR, *LPDESIGNVECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDESIGNVECTOR
 - wingdi/tagDESIGNVECTOR
 - PDESIGNVECTOR
 - wingdi/PDESIGNVECTOR
 - DESIGNVECTOR
 - wingdi/DESIGNVECTOR
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
 - DESIGNVECTOR
---

# DESIGNVECTOR structure


## -description

The <b>DESIGNVECTOR</b> structure is used by an application to specify values for the axes of a multiple master font.

## -struct-fields

### -field dvReserved

Reserved. Must be STAMP_DESIGNVECTOR.

### -field dvNumAxes

Number of values in the <b>dvValues</b> array.

### -field dvValues

An array specifying the values of the axes of a multiple master OpenType font. This array corresponds to the <b>axlAxisInfo</b> array in the <a href="/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a> structure.

## -remarks

The <b>dvNumAxes</b> member determines the actual size of <b>dvValues</b>, and thus, of <b>DESIGNVECTOR</b>. The constant MM_MAX_NUMAXES, which is 16, specifies the maximum allowed size of the <b>dvValues</b> array.

The PostScript Open Type Font does not support multiple master functionality.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontmemresourceex">AddFontMemResourceEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-addfontresourceexa">AddFontResourceEx</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-removefontresourceexa">RemoveFontResourceEx</a>