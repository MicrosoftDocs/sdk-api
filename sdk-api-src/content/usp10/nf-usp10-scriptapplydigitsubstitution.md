---
UID: NF:usp10.ScriptApplyDigitSubstitution
title: ScriptApplyDigitSubstitution function (usp10.h)
description: Applies the specified digit substitution settings to the specified script control and script state structures.
helpviewer_keywords: ["ScriptApplyDigitSubstitution","ScriptApplyDigitSubstitution function [Internationalization for Windows Applications]","_win32_ScriptApplyDigitSubstitution","intl.scriptapplydigitsubstitution","usp10/ScriptApplyDigitSubstitution"]
old-location: intl\scriptapplydigitsubstitution.htm
tech.root: Intl
ms.assetid: 486b8a56-eb14-48c3-b2f0-f5494f79baea
ms.date: 12/05/2018
ms.keywords: ScriptApplyDigitSubstitution, ScriptApplyDigitSubstitution function [Internationalization for Windows Applications], _win32_ScriptApplyDigitSubstitution, intl.scriptapplydigitsubstitution, usp10/ScriptApplyDigitSubstitution
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
 - ScriptApplyDigitSubstitution
 - usp10/ScriptApplyDigitSubstitution
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
 - ScriptApplyDigitSubstitution
---

# ScriptApplyDigitSubstitution function


## -description

Applies the specified digit substitution settings to the specified script control and script state structures.

## -parameters

### -param psds [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a> structure. The application sets this parameter to <b>NULL</b> if the function is to call <a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a> with LOCALE_USER_DEFAULT.

### -param psc [out]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> structure with the <b>fContextDigits</b> and <b>uDefaultLanguage</b> members updated.

### -param pss [out]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> structure with the <b>fDigitSubstitute</b> member updated.

## -returns

Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed.

The function returns E_INVALIDARG if it does not recognize the <b>DigitSubstitute</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a>.

## -remarks

This function does not actually substitute digits. It just fills in the structures that describe the digit substitution policy. See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>



<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>