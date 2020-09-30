---
UID: NF:usp10.ScriptRecordDigitSubstitution
title: ScriptRecordDigitSubstitution function (usp10.h)
description: Reads the National Language Support (NLS) native digit and digit substitution settings and records them in a SCRIPT_DIGITSUBSTITUTE structure. For more information, see Digit Shapes.
helpviewer_keywords: ["ScriptRecordDigitSubstitution","ScriptRecordDigitSubstitution function [Internationalization for Windows Applications]","_win32_ScriptRecordDigitSubstitution","intl.scriptrecorddigitsubstitution","usp10/ScriptRecordDigitSubstitution"]
old-location: intl\scriptrecorddigitsubstitution.htm
tech.root: Intl
ms.assetid: 2c8c33d5-5cd6-4734-bf44-af7d4b578672
ms.date: 12/05/2018
ms.keywords: ScriptRecordDigitSubstitution, ScriptRecordDigitSubstitution function [Internationalization for Windows Applications], _win32_ScriptRecordDigitSubstitution, intl.scriptrecorddigitsubstitution, usp10/ScriptRecordDigitSubstitution
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScriptRecordDigitSubstitution
 - usp10/ScriptRecordDigitSubstitution
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
 - ScriptRecordDigitSubstitution
---

# ScriptRecordDigitSubstitution function


## -description

Reads the National Language Support (NLS) native digit and digit substitution settings and records them in a <a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a> structure. For more information, see <a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>.

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> of the locale to query. Typically, the application should set this parameter to <a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>. Alternatively, the setting can indicate a specific locale combined with <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to obtain the default settings.

### -param psds [out]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a> structure. This structure can be passed later to <a href="/windows/desktop/api/usp10/nf-usp10-scriptapplydigitsubstitution">ScriptApplyDigitSubstitution</a>.

## -returns

Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed.

Error returns include:    
<ul>
<li>E_INVALIDARG. The <i>Locale</i> parameter indicates a locale that is invalid or not installed.</li>
<li>E_POINTER. The <i>psds</i> parameter is set to <b>NULL</b>.</li>
</ul>

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function supports context digit substitution only for Arabic and Persian locales. For other locales, context digit substitution is mapped to no substitution.

The following example shows the typical way to call this function.


```cpp
SCRIPT_DIGITSUBSTITUTE sds;
ScriptRecordDigitSubstitution(LOCALE_USER_DEFAULT, &sds);

```


At every itemization, the application can use the results as shown in the next example.


```cpp
SCRIPT_CONTROL sc = {0};
SCRIPT_STATE   ss = {0};
ScriptApplyDigitSubstitution(&sds, &sc, &ss);

```


For performance reasons, your application should not call <b>ScriptRecordDigitSubstitution</b> frequently. The function requires considerable overhead to call it every time <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> or <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a> is called. Instead, the application can save the <a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a> structure and update it only when a <a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message is received. Alternatively, the application can update the structure when a <a href="/windows/desktop/api/winreg/nf-winreg-regnotifychangekeyvalue">RegNotifyChangeKeyValue</a> call in a dedicated thread indicates a change in the registry under HKCU\Control Panel\International.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_digitsubstitute">SCRIPT_DIGITSUBSTITUTE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptapplydigitsubstitution">ScriptApplyDigitSubstitution</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptstringanalyse">ScriptStringAnalyse</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>