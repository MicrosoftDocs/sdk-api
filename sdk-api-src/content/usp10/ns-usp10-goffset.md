---
UID: NS:usp10.tagGOFFSET
title: GOFFSET (usp10.h)
description: Contains the x and y offsets of the combining glyph.
helpviewer_keywords: ["GOFFSET","GOFFSET structure [Internationalization for Windows Applications]","_win32_GOFFSET_str","intl.goffset","usp10/GOFFSET"]
old-location: intl\goffset.htm
tech.root: Intl
ms.assetid: 63fa8741-c8c8-480d-9702-2f4eb13bc01c
ms.date: 12/05/2018
ms.keywords: GOFFSET, GOFFSET structure [Internationalization for Windows Applications], _win32_GOFFSET_str, intl.goffset, usp10/GOFFSET
req.header: usp10.h
req.include-header: 
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
req.typenames: GOFFSET
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tagGOFFSET
 - usp10/tagGOFFSET
 - GOFFSET
 - usp10/GOFFSET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - GOFFSET
---

# GOFFSET structure


## -description

Contains the x and y offsets of the combining glyph.

## -struct-fields

### -field du

x offset, in logical units, for the combining glyph.

### -field dv

y offset, in logical units, for the combining glyph.

## -remarks

The members of this structure are named as they are so that they are not confused with the "dx" and "dy" designators for physical units in Uniscribe functions and structures.

## -see-also

<a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptpositionsingleglyph">ScriptPositionSingleGlyph</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>