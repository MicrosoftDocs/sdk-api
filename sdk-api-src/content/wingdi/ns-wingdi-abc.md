---
UID: NS:wingdi._ABC
title: ABC (wingdi.h)
description: The ABC structure contains the width of a character in a TrueType font.
helpviewer_keywords: ["*LPABC","*NPABC","*PABC","ABC","ABC structure [Windows GDI]","PABC","PABC structure pointer [Windows GDI]","_win32_ABC_str","gdi.abc","wingdi/ABC","wingdi/PABC"]
old-location: gdi\abc.htm
tech.root: gdi
ms.assetid: 00000000-0000-0000-0000-000000000001
ms.date: 12/05/2018
ms.keywords: '*LPABC, *NPABC, *PABC, ABC, ABC structure [Windows GDI], PABC, PABC structure pointer [Windows GDI], _win32_ABC_str, gdi.abc, wingdi/ABC, wingdi/PABC'
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
req.typenames: ABC, *PABC, *NPABC, *LPABC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ABC
 - wingdi/_ABC
 - PABC
 - wingdi/PABC
 - ABC
 - wingdi/ABC
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
 - ABC
---

# ABC structure


## -description

The <b>ABC</b> structure contains the width of a character in a TrueType font.

## -struct-fields

### -field abcA

The A spacing of the character. The A spacing is the distance to add to the current position before drawing the character glyph.

### -field abcB

The B spacing of the character. The B spacing is the width of the drawn portion of the character glyph.

### -field abcC

The C spacing of the character. The C spacing is the distance to add to the current position to provide white space to the right of the character glyph.

## -remarks

The total width of a character is the summation of the A, B, and C spaces. Either the A or the C space can be negative to indicate underhangs or overhangs.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>