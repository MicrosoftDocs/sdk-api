---
UID: NF:winnls.EnumSystemCodePagesA
title: EnumSystemCodePagesA function (winnls.h)
description: Enumerates the code pages that are either installed on or supported by an operating system. (ANSI)
helpviewer_keywords: ["CP_INSTALLED", "CP_SUPPORTED", "EnumSystemCodePagesA", "winnls/EnumSystemCodePagesA"]
old-location: intl\enumsystemcodepages.htm
tech.root: Intl
ms.assetid: 4ef4d30f-3e38-47ee-8f68-fbb286b7b5c3
ms.date: 12/05/2018
ms.keywords: CP_INSTALLED, CP_SUPPORTED, EnumSystemCodePages, EnumSystemCodePages function [Internationalization for Windows Applications], EnumSystemCodePagesA, EnumSystemCodePagesW, _win32_EnumSystemCodePages, intl.enumsystemcodepages, winnls/EnumSystemCodePages, winnls/EnumSystemCodePagesA, winnls/EnumSystemCodePagesW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumSystemCodePagesW (Unicode) and EnumSystemCodePagesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumSystemCodePagesA
 - winnls/EnumSystemCodePagesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumSystemCodePages
 - EnumSystemCodePagesA
 - EnumSystemCodePagesW
---

# EnumSystemCodePagesA function


## -description

Enumerates the code pages that are either installed on or supported by an operating system.

## -parameters

### -param lpCodePageEnumProc [in]

Pointer to an application-defined callback function. The <b>EnumSystemCodePages</b> function enumerates code pages by making repeated calls to this callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317809(v=vs.85)">EnumCodePagesProc</a>.

### -param dwFlags [in]

Flag specifying the code pages to enumerate. This parameter can have one of the following values, which are mutually exclusive.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_INSTALLED"></a><a id="cp_installed"></a><dl>
<dt><b>CP_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only installed code pages.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_SUPPORTED"></a><a id="cp_supported"></a><dl>
<dt><b>CP_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all supported code pages.

</td>
</tr>
</table>

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates the code pages by passing code page identifiers, one at a time, to the specified application-defined callback function. This process continues until all installed or supported code page identifiers have been passed to the callback function, or the callback function returns <b>FALSE</b>.

When an application is using this function to determine an appropriate code page for saving data, it should use Unicode when possible. Other code pages are not as portable as Unicode between vendors or operating systems, due to different implementations of the associated standards.





> [!NOTE]
> The winnls.h header defines EnumSystemCodePages as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd317809(v=vs.85)">EnumCodePagesProc</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
