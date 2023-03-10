---
UID: NF:usp10.ScriptStringValidate
title: ScriptStringValidate function (usp10.h)
description: Checks a SCRIPT_STRING_ANALYSIS structure for invalid sequences.
helpviewer_keywords: ["ScriptStringValidate","ScriptStringValidate function [Internationalization for Windows Applications]","_win32_ScriptStringValidate","intl.scriptstringvalidate","usp10/ScriptStringValidate"]
old-location: intl\scriptstringvalidate.htm
tech.root: Intl
ms.assetid: dde9332a-0a89-4914-9d41-6ce6519cdcb2
ms.date: 12/05/2018
ms.keywords: ScriptStringValidate, ScriptStringValidate function [Internationalization for Windows Applications], _win32_ScriptStringValidate, intl.scriptstringvalidate, usp10/ScriptStringValidate
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
 - ScriptStringValidate
 - usp10/ScriptStringValidate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptStringValidate
---

# ScriptStringValidate function


## -description

Checks a <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for invalid sequences.

## -parameters

### -param ssa [in]

A <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure for a string.

## -returns

Returns S_OK if no invalid sequences are found. The function returns S_FALSE if one or more invalid sequences are found. The function returns a nonzero HRESULT value if it does not succeed.

## -remarks

This function is intended for use in editors that reject the input of invalid sequences.

Invalid sequences are only checked for scripts with the <b>fRejectInvalid</b> member set in the associated <a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a> structure. For example, it is conventional for Notepad to reject invalid Thai character sequences. However, invalid Indian sequences are not conventionally rejected, but instead are displayed in composition with a missing base character symbol.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a>



<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>