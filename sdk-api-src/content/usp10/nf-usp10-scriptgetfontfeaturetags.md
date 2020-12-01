---
UID: NF:usp10.ScriptGetFontFeatureTags
title: ScriptGetFontFeatureTags function (usp10.h)
description: Retrieves a list of typographic features for the defined writing system for OpenType processing. The typographic feature tags comprising the list are retrieved from the font in the supplied device context or cache.
helpviewer_keywords: ["ScriptGetFontFeatureTags","ScriptGetFontFeatureTags function [Internationalization for Windows Applications]","_win32_ScriptGetFontFeatureTags","intl.scriptgetfontfeaturetags","usp10/ScriptGetFontFeatureTags"]
old-location: intl\scriptgetfontfeaturetags.htm
tech.root: Intl
ms.assetid: af3eb1e6-f402-4b99-b749-3ce8cef865b8
ms.date: 12/05/2018
ms.keywords: ScriptGetFontFeatureTags, ScriptGetFontFeatureTags function [Internationalization for Windows Applications], _win32_ScriptGetFontFeatureTags, intl.scriptgetfontfeaturetags, usp10/ScriptGetFontFeatureTags
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
 - ScriptGetFontFeatureTags
 - usp10/ScriptGetFontFeatureTags
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
 - ScriptGetFontFeatureTags
---

# ScriptGetFontFeatureTags function


## -description

Retrieves a list of typographic features for the defined writing system for OpenType processing. The typographic feature tags comprising the list are retrieved from the font in the supplied device context or cache.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param psa [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine, so that the font feature tags for the appropriate font and scripts can be retrieved.

Alternatively, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.

### -param tagScript [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the script tag associated with the specified feature tags.

### -param tagLangSys [in]

An <b>OPENTYPE_TAG</b> structure defining the language tag associated with the specified feature tags.

### -param cMaxTags [in]

The length of the array specified by <i>pFeatureTags</i>.

### -param pFeatureTags [out]

Pointer to a buffer in which this function retrieves an array of <b>OPENTYPE_TAG</b> structures defining the typographic feature tags supported by the font in the device context or cache for the defined writing system.

### -param pcTags [out]

Pointer to the number of elements in the feature tag array.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

If the number of matching tags exceeds the value of <i>cMaxTags</i>, the function fails with E_OUTOFMEMORY. The application can try calling again with larger buffers.

## -remarks

While formally declared as a ULONG type, an <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure contains a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z. For example, the feature tag for the Ligature feature is "liga".

This function hides script-required or language-required features because the shaping engine controls these features. The application has no control over the shaping engine handling for language-required features. For example, <b>ScriptGetFontFeatureTags</b> hides the Arabic script features for initial, medial, and final forms.

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