---
UID: NF:winnls.GetCPInfoExW
title: GetCPInfoExW function (winnls.h)
description: Retrieves information about any valid installed or available code page. (GetCPInfoExW)
helpviewer_keywords: ["CP_ACP", "CP_MACCP", "CP_OEMCP", "CP_THREAD_ACP", "GetCPInfoEx", "GetCPInfoEx function [Internationalization for Windows Applications]", "GetCPInfoExW", "_win32_GetCPInfoEx", "intl.getcpinfoex", "winnls/GetCPInfoEx", "winnls/GetCPInfoExW"]
old-location: intl\getcpinfoex.htm
tech.root: Intl
ms.assetid: c21ed6fe-85b6-438a-8f53-e30833e0c88a
ms.date: 12/05/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_THREAD_ACP, GetCPInfoEx, GetCPInfoEx function [Internationalization for Windows Applications], GetCPInfoExA, GetCPInfoExW, _win32_GetCPInfoEx, intl.getcpinfoex, winnls/GetCPInfoEx, winnls/GetCPInfoExA, winnls/GetCPInfoExW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCPInfoExW (Unicode) and GetCPInfoExA (ANSI)
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
 - GetCPInfoExW
 - winnls/GetCPInfoExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetCPInfoEx
 - GetCPInfoExA
 - GetCPInfoExW
---

# GetCPInfoExW function


## -description

Retrieves information about any valid installed or available code page.

## -parameters

### -param CodePage [in]

Identifier for the code page for which to retrieve information. The application can specify the code page identifier for any installed or available code page, or one of the following predefined values. See <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a> for a list of identifiers for ANSI and other code pages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_ACP"></a><a id="cp_acp"></a><dl>
<dt><b>CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default Windows ANSI code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_MACCP"></a><a id="cp_maccp"></a><dl>
<dt><b>CP_MACCP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default Macintosh code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_OEMCP"></a><a id="cp_oemcp"></a><dl>
<dt><b>CP_OEMCP</b></dt>
</dl>
</td>
<td width="60%">
Use the system default OEM code page.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_THREAD_ACP"></a><a id="cp_thread_acp"></a><dl>
<dt><b>CP_THREAD_ACP</b></dt>
</dl>
</td>
<td width="60%">
Use the current thread's ANSI code page.

</td>
</tr>
</table>

### -param dwFlags [in]

Reserved; must be 0.

### -param lpCPInfoEx [out]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-cpinfoexa">CPINFOEX</a> structure that receives information about the code page.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:


<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

The information retrieved in the <a href="/windows/desktop/api/winnls/ns-winnls-cpinfoexa">CPINFOEX</a> structure is not always useful for all code pages. To determine buffer sizes, for example, the application should call <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> or <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> to request an accurate buffer size. If <b>CPINFOEX</b> settings indicate that a lead byte exists, the conversion function does not necessarily handle lead bytes differently, for example, in the case of a missing or illegal trail byte.





> [!NOTE]
> The winnls.h header defines GetCPInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-cpinfoexa">CPINFOEX</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getacp">GetACP</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcpinfo">GetCPInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
