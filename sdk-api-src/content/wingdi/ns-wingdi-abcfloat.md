---
UID: NS:wingdi._ABCFLOAT
title: ABCFLOAT (wingdi.h)
description: The ABCFLOAT structure contains the A, B, and C widths of a font character.
old-location: gdi\abcfloat.htm
tech.root: gdi
ms.assetid: 540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0
ms.date: 12/05/2018
ms.keywords: '*LPABCFLOAT, *NPABCFLOAT, *PABCFLOAT, ABCFLOAT, ABCFLOAT structure [Windows GDI], PABCFLOAT, PABCFLOAT structure pointer [Windows GDI], _win32_ABCFLOAT_str, gdi.abcfloat, wingdi/ABCFLOAT, wingdi/PABCFLOAT'
f1_keywords:
- wingdi/ABCFLOAT
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
- ABCFLOAT
targetos: Windows
req.typenames: ABCFLOAT, *PABCFLOAT, *NPABCFLOAT, *LPABCFLOAT
req.redist: 
ms.custom: 19H1
---

# ABCFLOAT structure


## -description



The <b>ABCFLOAT</b> structure contains the A, B, and C widths of a font character.




## -struct-fields




### -field abcfA

The A spacing of the character. The A spacing is the distance to add to the current position before drawing the character glyph.


### -field abcfB

The B spacing of the character. The B spacing is the width of the drawn portion of the character glyph.


### -field abcfC

The C spacing of the character. The C spacing is the distance to add to the current position to provide white space to the right of the character glyph.


## -remarks



The A, B, and C widths are measured along the base line of the font.

The character increment (total width) of a character is the sum of the A, B, and C spaces. Either the A or the C space can be negative to indicate underhangs or overhangs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsfloata">GetCharABCWidthsFloat</a>
 

 

