---
UID: NS:usp10.script_charprop
title: SCRIPT_CHARPROP (usp10.h)
description: Contains information about a single character in a run (input string). The information indicates if the character glyph is affected by surrounding letters of the run.
helpviewer_keywords: ["SCRIPT_CHARPROP","SCRIPT_CHARPROP structure [Internationalization for Windows Applications]","_win32_SCRIPT_CHARPROP","intl.script_charprop","usp10/SCRIPT_CHARPROP"]
old-location: intl\script_charprop.htm
tech.root: Intl
ms.assetid: 2f3a4d8d-c7b1-4005-aebb-d3e9f2e3a37f
ms.date: 12/05/2018
ms.keywords: SCRIPT_CHARPROP, SCRIPT_CHARPROP structure [Internationalization for Windows Applications], _win32_SCRIPT_CHARPROP, intl.script_charprop, usp10/SCRIPT_CHARPROP
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SCRIPT_CHARPROP
req.redist: Usp10.dll version 1.600 or greater onWindows XP
ms.custom: 19H1
f1_keywords:
 - script_charprop
 - usp10/script_charprop
 - SCRIPT_CHARPROP
 - usp10/SCRIPT_CHARPROP
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
 - SCRIPT_CHARPROP
---

# SCRIPT_CHARPROP structure


## -description

Contains information about a single character in a run (input string). The information indicates if the character glyph is affected by surrounding letters of the run.

## -struct-fields

### -field fCanGlyphAlone

Value indicating if the shaping of a letter depends on other characters around the letter being shaped. Possible values are defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TRUE</td>
<td>The shape of a letter is independent of surrounding characters.</td>
</tr>
<tr>
<td>FALSE</td>
<td>The shape of a letter depends on one or more adjacent characters.</td>
</tr>
</table>

### -field reserved

Reserved.

## -remarks

One or more characters in a run, immediately preceding and/or following the letter being shaped, can influence shaping. Information about these characters can help optimize higher-level layout code, such as that used to optimize paragraph layout.


#### Examples

Let's look at an example of the use of this structure.



<ul>
<li>A font has ligatures for letter combinations "fi" and "fl", and no others. 
</li>
<li>The input string is "I like flying fish".</li>
<li> 
An array of <b>SCRIPT_CHARPROP</b> structures contains one structure for each character of the input string. 
</li>
</ul>
For the provided input string, the array of structures has the following values in the <b>fCanGlyphAlone</b> members:


```cpp
I like flying fish
111111100111110011

```

## -see-also

<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>