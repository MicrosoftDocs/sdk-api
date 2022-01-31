---
UID: NE:usp10.tag_SCRIPT_JUSTIFY
title: SCRIPT_JUSTIFY (usp10.h)
description: Defines glyph characteristic information that an application needs to implement justification.
helpviewer_keywords: ["SCRIPT_JUSTIFY","SCRIPT_JUSTIFY enumeration [Internationalization for Windows Applications]","SCRIPT_JUSTIFY_ARABIC_ALEF","SCRIPT_JUSTIFY_ARABIC_BA","SCRIPT_JUSTIFY_ARABIC_BARA","SCRIPT_JUSTIFY_ARABIC_BLANK","SCRIPT_JUSTIFY_ARABIC_HA","SCRIPT_JUSTIFY_ARABIC_KASHIDA","SCRIPT_JUSTIFY_ARABIC_NORMAL","SCRIPT_JUSTIFY_ARABIC_RA","SCRIPT_JUSTIFY_ARABIC_SEEN","SCRIPT_JUSTIFY_ARABIC_SEEN_M","SCRIPT_JUSTIFY_BLANK","SCRIPT_JUSTIFY_CHARACTER","SCRIPT_JUSTIFY_NONE","SCRIPT_JUSTIFY_RESERVED1","SCRIPT_JUSTIFY_RESERVED2","SCRIPT_JUSTIFY_RESERVED3","_win32_SCRIPT_JUSTIFY_str","intl.script_justify","usp10/SCRIPT_JUSTIFY","usp10/SCRIPT_JUSTIFY_ARABIC_ALEF","usp10/SCRIPT_JUSTIFY_ARABIC_BA","usp10/SCRIPT_JUSTIFY_ARABIC_BARA","usp10/SCRIPT_JUSTIFY_ARABIC_BLANK","usp10/SCRIPT_JUSTIFY_ARABIC_HA","usp10/SCRIPT_JUSTIFY_ARABIC_KASHIDA","usp10/SCRIPT_JUSTIFY_ARABIC_NORMAL","usp10/SCRIPT_JUSTIFY_ARABIC_RA","usp10/SCRIPT_JUSTIFY_ARABIC_SEEN","usp10/SCRIPT_JUSTIFY_ARABIC_SEEN_M","usp10/SCRIPT_JUSTIFY_BLANK","usp10/SCRIPT_JUSTIFY_CHARACTER","usp10/SCRIPT_JUSTIFY_NONE","usp10/SCRIPT_JUSTIFY_RESERVED1","usp10/SCRIPT_JUSTIFY_RESERVED2","usp10/SCRIPT_JUSTIFY_RESERVED3"]
old-location: intl\script_justify.htm
tech.root: Intl
ms.assetid: c2de8482-cca9-4ee3-b81a-8367fbe9130b
ms.date: 12/05/2018
ms.keywords: SCRIPT_JUSTIFY, SCRIPT_JUSTIFY enumeration [Internationalization for Windows Applications], SCRIPT_JUSTIFY_ARABIC_ALEF, SCRIPT_JUSTIFY_ARABIC_BA, SCRIPT_JUSTIFY_ARABIC_BARA, SCRIPT_JUSTIFY_ARABIC_BLANK, SCRIPT_JUSTIFY_ARABIC_HA, SCRIPT_JUSTIFY_ARABIC_KASHIDA, SCRIPT_JUSTIFY_ARABIC_NORMAL, SCRIPT_JUSTIFY_ARABIC_RA, SCRIPT_JUSTIFY_ARABIC_SEEN, SCRIPT_JUSTIFY_ARABIC_SEEN_M, SCRIPT_JUSTIFY_BLANK, SCRIPT_JUSTIFY_CHARACTER, SCRIPT_JUSTIFY_NONE, SCRIPT_JUSTIFY_RESERVED1, SCRIPT_JUSTIFY_RESERVED2, SCRIPT_JUSTIFY_RESERVED3, _win32_SCRIPT_JUSTIFY_str, intl.script_justify, usp10/SCRIPT_JUSTIFY, usp10/SCRIPT_JUSTIFY_ARABIC_ALEF, usp10/SCRIPT_JUSTIFY_ARABIC_BA, usp10/SCRIPT_JUSTIFY_ARABIC_BARA, usp10/SCRIPT_JUSTIFY_ARABIC_BLANK, usp10/SCRIPT_JUSTIFY_ARABIC_HA, usp10/SCRIPT_JUSTIFY_ARABIC_KASHIDA, usp10/SCRIPT_JUSTIFY_ARABIC_NORMAL, usp10/SCRIPT_JUSTIFY_ARABIC_RA, usp10/SCRIPT_JUSTIFY_ARABIC_SEEN, usp10/SCRIPT_JUSTIFY_ARABIC_SEEN_M, usp10/SCRIPT_JUSTIFY_BLANK, usp10/SCRIPT_JUSTIFY_CHARACTER, usp10/SCRIPT_JUSTIFY_NONE, usp10/SCRIPT_JUSTIFY_RESERVED1, usp10/SCRIPT_JUSTIFY_RESERVED2, usp10/SCRIPT_JUSTIFY_RESERVED3
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
req.typenames: SCRIPT_JUSTIFY
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_JUSTIFY
 - usp10/tag_SCRIPT_JUSTIFY
 - SCRIPT_JUSTIFY
 - usp10/SCRIPT_JUSTIFY
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
 - SCRIPT_JUSTIFY
---

# SCRIPT_JUSTIFY enumeration


## -description

Defines glyph characteristic information that an application needs to implement justification.

## -enum-fields

### -field SCRIPT_JUSTIFY_NONE:0

Justification cannot be applied at the glyph.

### -field SCRIPT_JUSTIFY_ARABIC_BLANK:1

The glyph represents a blank in an Arabic run.

### -field SCRIPT_JUSTIFY_CHARACTER:2

An inter-character justification point follows the glyph.

### -field SCRIPT_JUSTIFY_RESERVED1:3

Reserved.

### -field SCRIPT_JUSTIFY_BLANK:4

The glyph represents a blank outside an Arabic run.

### -field SCRIPT_JUSTIFY_RESERVED2:5

Reserved.

### -field SCRIPT_JUSTIFY_RESERVED3:6

Reserved.

### -field SCRIPT_JUSTIFY_ARABIC_NORMAL:7

Normal middle-of-word glyph that connects to the right (begin).

### -field SCRIPT_JUSTIFY_ARABIC_KASHIDA:8

Kashida (U+0640) in the middle of the word.

### -field SCRIPT_JUSTIFY_ARABIC_ALEF:9

Final form of an alef-like (U+0627, U+0625, U+0623, U+0622).

### -field SCRIPT_JUSTIFY_ARABIC_HA:10

Final form of Ha (U+0647).

### -field SCRIPT_JUSTIFY_ARABIC_RA:11

Final form of Ra (U+0631).

### -field SCRIPT_JUSTIFY_ARABIC_BA:12

Final form of Ba (U+0628).

### -field SCRIPT_JUSTIFY_ARABIC_BARA:13

Ligature of alike (U+0628,U+0631).

### -field SCRIPT_JUSTIFY_ARABIC_SEEN:14

Highest priority: initial shape of Seen class (U+0633).

### -field SCRIPT_JUSTIFY_ARABIC_SEEN_M:15

Highest priority: medial shape of Seen class (U+0633).

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-enumeration-types">Uniscribe Enumeration Types</a>
