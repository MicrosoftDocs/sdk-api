---
UID: NF:gb18030.NlsDllCodePageTranslation
title: NlsDllCodePageTranslation function (gb18030.h)
description: Used to get code page information or do conversion, depending on flag settings.
helpviewer_keywords: ["NLS_CP_CPINFO","NLS_CP_MBTOWC","NLS_CP_WCTOMB","NlsDllCodePageTranslation","NlsDllCodePageTranslation function [Internationalization for Windows Applications]","_win32_NlsDllCodePageTranslation","gb18030/NlsDllCodePageTranslation","intl.nlsdllcodepagetranslation"]
old-location: intl\nlsdllcodepagetranslation.htm
tech.root: Intl
ms.assetid: cc653877-de16-4ccc-b48e-8bd7cfacb43c
ms.date: 12/05/2018
ms.keywords: NLS_CP_CPINFO, NLS_CP_MBTOWC, NLS_CP_WCTOMB, NlsDllCodePageTranslation, NlsDllCodePageTranslation function [Internationalization for Windows Applications], _win32_NlsDllCodePageTranslation, gb18030/NlsDllCodePageTranslation, intl.nlsdllcodepagetranslation
req.header: gb18030.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: C_g18030.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NlsDllCodePageTranslation
 - gb18030/NlsDllCodePageTranslation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - C_g18030.dll
api_name:
 - NlsDllCodePageTranslation
---

# NlsDllCodePageTranslation function


## -description

Used to get code page information or do conversion, depending on flag settings.


<div class="alert"><b>Note</b>  Do not use this function. It can behave differently in different versions of Windows. To convert GB18030 bytes to Unicode characters or Unicode characters to GB18030 bytes, use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions.</div>
<div> </div>

## -parameters

### -param CodePage [in]

The value of the code page. The code page value should be 54936. Otherwise, the function returns an error code.

### -param dwFlags [in]

Flags specifying the translation. Possible values are defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NLS_CP_CPINFO"></a><a id="nls_cp_cpinfo"></a><dl>
<dt><b>NLS_CP_CPINFO</b></dt>
</dl>
</td>
<td width="60%">
Retrieve code page information in the buffer pointed to by <i>lpCPInfo</i>. The <i>lpMultiByteStr</i>, <i>cchMultiByte</i>, <i>lpWideCharStr</i>, and <i>cchWideChar</i> parameters are not used.

</td>
</tr>
<tr>
<td width="40%"><a id="NLS_CP_MBTOWC"></a><a id="nls_cp_mbtowc"></a><dl>
<dt><b>NLS_CP_MBTOWC</b></dt>
</dl>
</td>
<td width="60%">
Convert GB18030 bytes to Unicode characters. The source GB18030 characters should be pointed to by <i>lpMultiByteStr</i>, and <i>cchMultiByte</i> should contain the byte count of the buffer. The Unicode result is stored in the buffer pointed to by <i>lpWideCharStr</i>, and <i>cchWideChar</i> should contain the character count of the Unicode buffer. If <i>lpWideCharStr</i> or <i>cchWideChar</i> is 0, the expected character count of the Unicode result is returned, and no conversion is done. The <i>lpCPInfo</i> parameter is not used in this case.

</td>
</tr>
<tr>
<td width="40%"><a id="NLS_CP_WCTOMB"></a><a id="nls_cp_wctomb"></a><dl>
<dt><b>NLS_CP_WCTOMB</b></dt>
</dl>
</td>
<td width="60%">
Convert Unicode characters to GB18030 bytes. The source Unicode string should be pointed to by <i>lpWideCharStr</i>, and <i>cchWideChar</i> should contain the character count of the buffer. The GB18030 result is stored in the buffer pointed to by <i>lpMultiByteStr</i>, and <i>cchMultiByte</i> should contain the byte count of the GB18030 buffer. If <i>lpMultiByteStr</i> or <i>cchMultiByte</i> is 0, the byte count of the GB18030 result is returned, and no conversion is done. The <i>lpCPInfo</i> parameter is not used in this case.

</td>
</tr>
</table>

### -param lpMultiByteStr [in, out]

Pointer to a buffer that contains multibyte GB18030 characters. This can be a source buffer or target buffer, depending on the value of <i>dwFlags</i>.

### -param cchMultiByte [in]

Byte count of the multibyte buffer.

### -param lpWideCharStr [in, out]

Pointer to a buffer that contains Unicode characters. This can be a source buffer or target buffer, depending on the value of <i>dwFlags</i>.

### -param cchWideChar [in]

Character count of the Unicode buffer.

### -param lpCPInfo [in]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-cpinfo">CPINFO</a> structure.

## -returns

Returns 1 if successful. If the function does not succeed, it returns 0. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:


<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>