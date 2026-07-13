---
UID: NF:winnls.GetOEMCP
title: GetOEMCP function (winnls.h)
description: Returns the current original equipment manufacturer (OEM) code page identifier for the operating system.
helpviewer_keywords: ["GetOEMCP","GetOEMCP function [Internationalization for Windows Applications]","_win32_GetOEMCP","intl.getoemcp","winnls/GetOEMCP"]
old-location: intl\getoemcp.htm
tech.root: Intl
ms.assetid: e6d42641-4bbe-44d8-baea-1087e48dae7d
ms.date: 12/05/2018
ms.keywords: GetOEMCP, GetOEMCP function [Internationalization for Windows Applications], _win32_GetOEMCP, intl.getoemcp, winnls/GetOEMCP
req.header: winnls.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOEMCP
 - winnls/GetOEMCP
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
 - GetOEMCP
---

# GetOEMCP function


## -description

Returns the current original equipment manufacturer (OEM) code page identifier for the operating system.
<div class="alert"><b>Note</b>   The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use Unicode, such as UTF-8 or UTF-16, instead of a specific code page.</div><div> </div>



## -returns

Returns the current OEM code page identifier for the operating system.

## -remarks

See <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a> for a list of OEM and other code pages.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getacp">GetACP</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
