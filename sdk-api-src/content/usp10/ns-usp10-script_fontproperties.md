---
UID: NS:usp10.SCRIPT_FONTPROPERTIES
title: SCRIPT_FONTPROPERTIES (usp10.h)
description: Contains information about the properties of the current font.
helpviewer_keywords: ["SCRIPT_FONTPROPERTIES","SCRIPT_FONTPROPERTIES structure [Internationalization for Windows Applications]","_win32_SCRIPT_FONTPROPERTIES_str","intl.script_fontproperties","usp10/SCRIPT_FONTPROPERTIES"]
old-location: intl\script_fontproperties.htm
tech.root: Intl
ms.assetid: 6757e758-6525-47a4-9ed4-99ef42fa14a3
ms.date: 12/05/2018
ms.keywords: SCRIPT_FONTPROPERTIES, SCRIPT_FONTPROPERTIES structure [Internationalization for Windows Applications], _win32_SCRIPT_FONTPROPERTIES_str, intl.script_fontproperties, usp10/SCRIPT_FONTPROPERTIES
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
req.typenames: SCRIPT_FONTPROPERTIES
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - SCRIPT_FONTPROPERTIES
 - usp10/SCRIPT_FONTPROPERTIES
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
 - SCRIPT_FONTPROPERTIES
---

# SCRIPT_FONTPROPERTIES structure


## -description

Contains information about the properties of the current font.

## -struct-fields

### -field cBytes

Size, in bytes, of the structure.

### -field wgBlank

Glyph used to indicate a blank.

### -field wgDefault

Glyph used to indicate Unicode characters not present in the font.

### -field wgInvalid

Glyph used to indicate invalid character combinations.

### -field wgKashida

Glyph used to indicate the shortest continuous kashida, with 1 indicating that the font contains no kashida.

### -field iKashidaWidth

Width of the shortest continuous kashida glyph in the font, indicated by the <b>wgKashida</b> member.

## -see-also

<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>

