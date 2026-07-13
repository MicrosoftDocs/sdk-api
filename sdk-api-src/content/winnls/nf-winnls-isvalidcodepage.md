---
UID: NF:winnls.IsValidCodePage
title: IsValidCodePage function (winnls.h)
description: Determines if a specified code page is valid.
helpviewer_keywords: ["IsValidCodePage","IsValidCodePage function [Internationalization for Windows Applications]","_win32_IsValidCodePage","intl.isvalidcodepage","winnls/IsValidCodePage"]
old-location: intl\isvalidcodepage.htm
tech.root: Intl
ms.assetid: 7bd16f61-a534-4ada-ae27-d5deb47870a9
ms.date: 12/05/2018
ms.keywords: IsValidCodePage, IsValidCodePage function [Internationalization for Windows Applications], _win32_IsValidCodePage, intl.isvalidcodepage, winnls/IsValidCodePage
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
 - IsValidCodePage
 - winnls/IsValidCodePage
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
 - IsValidCodePage
---

# IsValidCodePage function


## -description

Determines if a specified code page is valid.

## -parameters

### -param CodePage [in]

<a href="/windows/desktop/Intl/code-page-identifiers">Code page identifier</a> for the code page to check.

## -returns

Returns a nonzero value if the code page is valid, or 0 if the code page is invalid.

## -remarks

A code page is considered valid only if it is installed on the operating system. Unicode is preferred.

Starting with Windows Vista, all code pages that can be installed are loaded by default.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getacp">GetACP</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcpinfo">GetCPInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>