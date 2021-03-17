---
UID: NF:wingdi.SetTextCharacterExtra
title: SetTextCharacterExtra function (wingdi.h)
description: The SetTextCharacterExtra function sets the intercharacter spacing. Intercharacter spacing is added to each character, including break characters, when the system writes a line of text.
helpviewer_keywords: ["SetTextCharacterExtra","SetTextCharacterExtra function [Windows GDI]","_win32_SetTextCharacterExtra","gdi.settextcharacterextra","wingdi/SetTextCharacterExtra"]
old-location: gdi\settextcharacterextra.htm
tech.root: gdi
ms.assetid: 83b7d225-4fb9-4c75-bc4a-e1bea7f901f1
ms.date: 12/05/2018
ms.keywords: SetTextCharacterExtra, SetTextCharacterExtra function [Windows GDI], _win32_SetTextCharacterExtra, gdi.settextcharacterextra, wingdi/SetTextCharacterExtra
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetTextCharacterExtra
 - wingdi/SetTextCharacterExtra
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetTextCharacterExtra
---

# SetTextCharacterExtra function


## -description

The <b>SetTextCharacterExtra</b> function sets the intercharacter spacing. Intercharacter spacing is added to each character, including break characters, when the system writes a line of text.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param extra [in]

The amount of extra space, in logical units, to be added to each character. If the current mapping mode is not MM_TEXT, the <i>nCharExtra</i> parameter is transformed and rounded to the nearest pixel.

## -returns

If the function succeeds, the return value is the previous intercharacter spacing.

If the function fails, the return value is 0x80000000.

## -remarks

This function is supported mainly for compatibility with existing applications. New applications should generally avoid calling this function, because it is incompatible with complex scripts (scripts that require text shaping; Arabic script is an example of this).

The recommended approach is that instead of calling this function and then <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>, applications should call <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> and use its <i>lpDx</i> parameter to supply widths.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcharacterextra">GetTextCharacterExtra</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>