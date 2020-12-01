---
UID: NF:usp10.ScriptGetGlyphABCWidth
title: ScriptGetGlyphABCWidth function (usp10.h)
description: Retrieves the ABC width of a given glyph.
helpviewer_keywords: ["ScriptGetGlyphABCWidth","ScriptGetGlyphABCWidth function [Internationalization for Windows Applications]","_win32_ScriptGetGlyphABCWidth","intl.scriptgetglyphabcwidth","usp10/ScriptGetGlyphABCWidth"]
old-location: intl\scriptgetglyphabcwidth.htm
tech.root: Intl
ms.assetid: 71611c9c-f8f6-4064-b153-f31a8cbb7761
ms.date: 12/05/2018
ms.keywords: ScriptGetGlyphABCWidth, ScriptGetGlyphABCWidth function [Internationalization for Windows Applications], _win32_ScriptGetGlyphABCWidth, intl.scriptgetglyphabcwidth, usp10/ScriptGetGlyphABCWidth
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptGetGlyphABCWidth
 - usp10/ScriptGetGlyphABCWidth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetGlyphABCWidth
---

# ScriptGetGlyphABCWidth function


## -description

Retrieves the <a href="/windows/desktop/Intl/uniscribe-glossary">ABC width</a> of a given glyph.

## -parameters

### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param wGlyph [in]

Glyph to analyze.

### -param pABC [out]

Pointer to the ABC width of the specified glyph.

## -returns

Returns S_OK if the ABC width of the glyph is retrieved. The function returns a nonzero HRESULT value if it does not succeed.

The function returns E_HANDLE if the font or operating system does not support glyph indexes.

## -remarks

This function is limited in its usefulness. For example, it is useful for drawing glyph charts. It should not be used for ordinary complex script text formatting.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>