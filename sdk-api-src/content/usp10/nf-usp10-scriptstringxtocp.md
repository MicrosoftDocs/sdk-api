---
UID: NF:usp10.ScriptStringXtoCP
title: ScriptStringXtoCP function (usp10.h)
description: Converts an x coordinate to a character position.
helpviewer_keywords: ["ScriptStringXtoCP","ScriptStringXtoCP function [Internationalization for Windows Applications]","_win32_ScriptStringXtoCP","intl.scriptstringxtocp","usp10/ScriptStringXtoCP"]
old-location: intl\scriptstringxtocp.htm
tech.root: Intl
ms.assetid: ae37f58a-cc9c-4414-a8ac-e70691e54c5e
ms.date: 12/05/2018
ms.keywords: ScriptStringXtoCP, ScriptStringXtoCP function [Internationalization for Windows Applications], _win32_ScriptStringXtoCP, intl.scriptstringxtocp, usp10/ScriptStringXtoCP
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
 - ScriptStringXtoCP
 - usp10/ScriptStringXtoCP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptStringXtoCP
---

# ScriptStringXtoCP function


## -description

Converts an x coordinate to a character position.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for the string.

### -param iX [in]

The x coordinate.

### -param piCh [out]

Pointer to a variable in which this function retrieves the character position corresponding to the x coordinate.

### -param piTrailing [out]

Pointer to a variable in which this function retrieves a value indicating if the x coordinate is for the leading edge or the trailing edge of the character position. For more information, see the Remarks section.

## -returns

Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

If the x coordinate corresponds to the leading edge of the character, the value of <i>piTrailing</i> is 0. If the x coordinate corresponds to the trailing edge of the character, the value of <i>piTrailing</i> is a positive integer. As for <a href="/windows/desktop/api/usp10/nf-usp10-scriptxtocp">ScriptXtoCP</a>, the value is 1 for a character that can be rendered on its own. The value is greater than 1 if the character is part of a cluster in a script for which cursors are not placed within a cluster, to indicate the offset to the next legitimate logical cursor position.

If the x coordinate is before the beginning of the line, the function retrieves -1 for <i>piCh</i> and 1 for <i>piTrailing</i>, indicating the trailing edge of the nonexistent character before the line. If the x coordinate is after the end of the line, the function retrieves for <i>piCh</i> the first index beyond the length of the line and 0 for <i>piTrailing</i>. The 0 value indicates the leading edge of the nonexistent character after the line.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>