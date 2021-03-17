---
UID: NF:usp10.ScriptGetFontLanguageTags
title: ScriptGetFontLanguageTags function (usp10.h)
description: Retrieves a list of language tags that are available for the specified item and are supported by a specified script tag for OpenType processing. The tags comprising the list are retrieved from the font in the specified device context or cache.
helpviewer_keywords: ["ScriptGetFontLanguageTags","ScriptGetFontLanguageTags function [Internationalization for Windows Applications]","_win32_ScriptGetFontLanguageTags","intl.scriptgetfontlanguagetags","usp10/ScriptGetFontLanguageTags"]
old-location: intl\scriptgetfontlanguagetags.htm
tech.root: Intl
ms.assetid: 554915f0-4bfc-4777-98cd-c2bee6ac4ef4
ms.date: 12/05/2018
ms.keywords: ScriptGetFontLanguageTags, ScriptGetFontLanguageTags function [Internationalization for Windows Applications], _win32_ScriptGetFontLanguageTags, intl.scriptgetfontlanguagetags, usp10/ScriptGetFontLanguageTags
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
f1_keywords:
 - ScriptGetFontLanguageTags
 - usp10/ScriptGetFontLanguageTags
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
 - ScriptGetFontLanguageTags
---

# ScriptGetFontLanguageTags function


## -description

Retrieves a list of language tags that are available for the specified item and are supported by a specified script tag for OpenType processing. The tags comprising the list are retrieved from the font in the specified device context or cache.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param psa [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine, so that the font language tags for the appropriate font and scripts can be retrieved.

Alternately, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.

### -param tagScript [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the script tag for which the list of associated language tags is requested.

### -param cMaxTags [in]

The length of the array specified by <i>pLangSysTags</i>.

### -param pLangsysTags [out]

Pointer to a buffer in which this function retrieves an array of <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structures identifying the language tags matching input criteria.

### -param pcTags [out]

Pointer to the number of elements in the language tag array.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

If the number of matching tags exceeds <i>cMaxTags</i>, the function fails with E_OUTOFMEMORY. The application can try calling again with larger buffers.

## -remarks

While formally declared as a ULONG type, the <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure contains a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z. For example, the language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively. Note that each tag ends with a space.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/caching">Caching</a>



<a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>