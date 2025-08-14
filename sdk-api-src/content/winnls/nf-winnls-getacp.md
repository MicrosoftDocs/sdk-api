---
UID: NF:winnls.GetACP
title: GetACP function (winnls.h)
description: Retrieves the current Windows ANSI code page identifier for the operating system.Caution  The ANSI API functions, for example, the ANSI version of TextOut, implicitly use GetACP to translate text to or from Unicode.
helpviewer_keywords: ["GetACP","GetACP function [Internationalization for Windows Applications]","_win32_GetACP","intl.getacp","winnls/GetACP"]
old-location: intl\getacp.htm
tech.root: Intl
ms.assetid: a28c3f08-ee76-4e3f-b14d-fabc0af98fef
ms.date: 12/05/2018
ms.keywords: GetACP, GetACP function [Internationalization for Windows Applications], _win32_GetACP, intl.getacp, winnls/GetACP
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
 - GetACP
 - winnls/GetACP
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
 - GetACP
---

# GetACP function


## -description

Retrieves the current Windows ANSI code page identifier for the operating system.<div class="alert"><b>Caution</b>  The ANSI API functions, for example, the ANSI version of <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>, implicitly use <b>GetACP</b> to translate text to or from Unicode. For the Multilingual User Interface (MUI) edition of Windows, the system ACP might not cover all code points in the user's selected logon language identifier. For compatibility with this edition, your application should avoid calls that depend on <b>GetACP</b> either implicitly or explicitly, as this function can cause some locales to display text as question marks. Instead, the application should use the Unicode API functions directly, for example, the Unicode version of <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>.</div>
<div> </div>



## -returns

Returns the current Windows ANSI code page (ACP) identifier for the operating system. See <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a> for a list of identifiers for Windows ANSI code pages and other code pages.

## -remarks

The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use UTF-8 or UTF-16 when possible.

## -see-also

<a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcpinfo">GetCPInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
