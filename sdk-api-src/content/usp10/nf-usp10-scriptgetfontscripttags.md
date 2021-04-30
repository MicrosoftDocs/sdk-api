---
UID: NF:usp10.ScriptGetFontScriptTags
title: ScriptGetFontScriptTags function (usp10.h)
description: Retrieves a list of scripts available in the font for OpenType processing. Scripts comprising the list are retrieved from the font located in the supplied device context or from the script shaping engine that processes the font of the current run.
helpviewer_keywords: ["ScriptGetFontScriptTags","ScriptGetFontScriptTags function [Internationalization for Windows Applications]","_win32_ScriptGetFontScriptTags","intl.scriptgetfontscripttags","usp10/ScriptGetFontScriptTags"]
old-location: intl\scriptgetfontscripttags.htm
tech.root: Intl
ms.assetid: d93dd2d6-93c5-4781-8645-fd3f0b45c9b7
ms.date: 12/05/2018
ms.keywords: ScriptGetFontScriptTags, ScriptGetFontScriptTags function [Internationalization for Windows Applications], _win32_ScriptGetFontScriptTags, intl.scriptgetfontscripttags, usp10/ScriptGetFontScriptTags
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
 - ScriptGetFontScriptTags
 - usp10/ScriptGetFontScriptTags
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
 - ScriptGetFontScriptTags
---

# ScriptGetFontScriptTags function


## -description

Retrieves a list of scripts available in the font for OpenType processing. Scripts comprising the list are retrieved from the font located in the supplied device context or from the script shaping engine that processes the font of the current run.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param psa [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. This parameter identifies the shaping engine, so that the appropriate font script tags can be retrieved. The application supplies a non-<b>NULL</b> value for this parameter to retrieve script tags appropriate for the current run.

Alternatively, the application can set this parameter to <b>NULL</b> to retrieve unfiltered results.

### -param cMaxTags [in]

The length of the array specified by <i>pScriptTags</i>.

### -param pScriptTags [out]

Pointer to a buffer in which this function retrieves an array of <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structures defining script tags from the device context or the scripting engine associated with the current run. If the value of the <b>eScript</b> member of the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure provided in the <i>psa</i> parameter has a definite script tag associated with it and the tag is present in the font, <i>pScriptTags</i> contains only this tag.

### -param pcTags [out]

Pointer to the number of elements in the script tag array indicated by <i>pScriptTags</i>.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

If the number of matching tags exceeds the value of <i>cMaxTags</i>, the function fails with E_OUTOFMEMORY. The application can try calling again with larger buffers.

## -remarks

While formally declared as a ULONG type, <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z or a-z. For example, the script tags for Latin and Arabic scripts are "latn" and "arab", respectively.

This function retrieves a single tag from a font in the following cases:

<ul>
<li>The <i>psa</i> value is associated with text for a single complex script.</li>
<li>The <i>psa</i> parameter indicates <b>NULL</b> and the font supports a single script.</li>
</ul>
If <b>ScriptGetFontScriptTags</b> retrieves all tags from a font, the tags are usually for neutral items, such as digits. Note that more than one tag might be applicable because some text runs of neutral items are not script-specific.

If a tag corresponding to a particular script is present, a shaping engine might be unable to use the font to shape the given item because the engine lacks a needed item, such as a specific language system or a specific feature.

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