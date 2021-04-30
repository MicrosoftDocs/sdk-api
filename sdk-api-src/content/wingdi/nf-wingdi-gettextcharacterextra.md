---
UID: NF:wingdi.GetTextCharacterExtra
title: GetTextCharacterExtra function (wingdi.h)
description: The GetTextCharacterExtra function retrieves the current intercharacter spacing for the specified device context.
helpviewer_keywords: ["GetTextCharacterExtra","GetTextCharacterExtra function [Windows GDI]","_win32_GetTextCharacterExtra","gdi.gettextcharacterextra","wingdi/GetTextCharacterExtra"]
old-location: gdi\gettextcharacterextra.htm
tech.root: gdi
ms.assetid: 44d5145d-1c42-429e-89c4-dc31d275bc73
ms.date: 12/05/2018
ms.keywords: GetTextCharacterExtra, GetTextCharacterExtra function [Windows GDI], _win32_GetTextCharacterExtra, gdi.gettextcharacterextra, wingdi/GetTextCharacterExtra
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
 - GetTextCharacterExtra
 - wingdi/GetTextCharacterExtra
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextCharacterExtra
---

# GetTextCharacterExtra function


## -description

The <b>GetTextCharacterExtra</b> function retrieves the current intercharacter spacing for the specified device context.

## -parameters

### -param hdc [in]

Handle to the device context.

## -returns

If the function succeeds, the return value is the current intercharacter spacing, in logical coordinates.

If the function fails, the return value is 0x8000000.

## -remarks

The intercharacter spacing defines the extra space, in logical units along the base line, that the <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> functions add to each character as a line is written. The spacing is used to expand lines of text.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>