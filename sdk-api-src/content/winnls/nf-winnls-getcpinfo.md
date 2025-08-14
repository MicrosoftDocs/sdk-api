---
UID: NF:winnls.GetCPInfo
title: GetCPInfo function (winnls.h)
description: Retrieves information about any valid installed or available code page. (GetCPInfo)
helpviewer_keywords: ["GetCPInfo","GetCPInfo function [Internationalization for Windows Applications]","_win32_GetCPInfo","intl.getcpinfo","winnls/GetCPInfo"]
old-location: intl\getcpinfo.htm
tech.root: Intl
ms.assetid: f7401cd5-d0ed-49b1-b8fc-dda8df99e6b6
ms.date: 12/05/2018
ms.keywords: GetCPInfo, GetCPInfo function [Internationalization for Windows Applications], _win32_GetCPInfo, intl.getcpinfo, winnls/GetCPInfo
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - GetCPInfo
 - winnls/GetCPInfo
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
api_name:
 - GetCPInfo
---

# GetCPInfo function


## -description

Retrieves information about any valid installed or available code page. 
<div class="alert"><b>Note</b>  To obtain additional information about valid installed or available code pages, the application should use <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a>.</div><div> </div>

## -parameters

### -param CodePage [in]

Identifier for the code page for which to retrieve information. For details, see the <i>CodePage</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a>.

### -param lpCPInfo [out]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-cpinfo">CPINFO</a> structure that receives information about the code page. See the Remarks section.

## -returns

Returns 1 if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:
				

<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a>.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-cpinfo">CPINFO</a>



<a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getacp">GetACP</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>
