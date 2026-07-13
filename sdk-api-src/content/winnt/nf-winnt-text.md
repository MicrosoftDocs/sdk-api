---
UID: NF:winnt.TEXT
title: TEXT macro (winnt.h)
description: Identifies a string as Unicode when UNICODE is defined by a preprocessor directive during compilation. Otherwise, the macro identifies a string as an ANSI string.
helpviewer_keywords: ["TEXT","TEXT macro [Internationalization for Windows Applications]","_win32_TEXT_Macro","intl.text","winnt/TEXT"]
old-location: intl\text.htm
tech.root: Intl
ms.assetid: 427d365f-2277-460c-8120-3ccb6c6cea4f
ms.date: 07/01/2025
ms.keywords: TEXT, TEXT macro [Internationalization for Windows Applications], _win32_TEXT_Macro, intl.text, winnt/TEXT
req.header: winnt.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TEXT
 - winnt/TEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TEXT
---

# TEXT macro

## -syntax

```cpp
void TEXT(
    LPTSTR quote
);
```


## -description

Identifies a string as Unicode when UNICODE is defined by a preprocessor directive during compilation. Otherwise, the macro identifies a string as an ANSI string.

## -parameters

### -param quote

Pointer to the string to interpret as UTF-16 or ANSI.

## -remarks

This macro interprets an ANSI string at runtime according to the current Windows ANSI code page. Literal ANSI strings that are not strictly ASCII are interpreted differently when processed with different Windows ANSI code pages. For example, "\0xC4" in code page 1252 (Latin-1) represents Upper Case A with Dieresis (Ä). However, in code page 1253 (Greek), the string represents Upper Case Delta (Δ). These different interpretations lead to development and maintenance issues. For example, a developer might correct a string when using a different system code page from the page used by the original developer; or a build computer might use a different code page. The different interpretations also pose runtime issues, for example, when the end user computer uses a different code page to interpret a string from that used by the build computer.

## -see-also

<a href="/windows/desktop/Intl/unicode-and-character-set-macros">Unicode and Character Set Macros</a>



<a href="/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>
