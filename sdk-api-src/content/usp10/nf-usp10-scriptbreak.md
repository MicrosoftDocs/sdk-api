---
UID: NF:usp10.ScriptBreak
title: ScriptBreak function (usp10.h)
description: Retrieves information for determining line breaks.
helpviewer_keywords: ["ScriptBreak","ScriptBreak function [Internationalization for Windows Applications]","_win32_ScriptBreak","intl.scriptbreak","usp10/ScriptBreak"]
old-location: intl\scriptbreak.htm
tech.root: Intl
ms.assetid: 1613819f-9473-4d9f-8a65-a109c9ef3f43
ms.date: 12/05/2018
ms.keywords: ScriptBreak, ScriptBreak function [Internationalization for Windows Applications], _win32_ScriptBreak, intl.scriptbreak, usp10/ScriptBreak
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
 - ScriptBreak
 - usp10/ScriptBreak
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptBreak
---

# ScriptBreak function


## -description

Retrieves information for determining line breaks.

## -parameters

### -param pwcChars [in]

Pointer to the Unicode characters to process.

### -param cChars [in]

Number of Unicode characters to process.

### -param psa [in]

Pointer to the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from an earlier call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>.

### -param psla [out]

Pointer to a buffer in which this function retrieves the character attributes as a <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> structure.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function does not require a device context and does not perform glyph shaping.

This function retrieves cursor movement and formatting break positions for an item in an array of <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> structures. To support mixed formatting within a single word correctly, the call to <b>ScriptBreak</b> should pass whole items as retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>, and not the finer formatting runs.

The <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> structure identifies valid caret positions and line breaks. The <b>fCharStop</b> member specifies a flag that marks cluster boundaries for scripts that are conventionally restricted from moving inside clusters. The same boundaries can also be inferred by inspecting the logical cluster information retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>. However, <b>ScriptBreak</b> is considerably faster in implementation and does not require a device context to be prepared.

The flags designated by the <b>fWordStop</b>, <b>fSoftBreak</b>, and <b>fWhiteSpace</b> members of <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> are only available through <b>ScriptBreak</b>.

Most shaping engines that identify invalid sequences set the flag indicated by the <b>fInvalid</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a> in <b>ScriptBreak</b>. The <b>fInvalidLogAttr</b> member of <a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a> identifies the applicable scripts.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>