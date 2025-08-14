---
UID: NF:winnls.GetSystemDefaultLangID
title: GetSystemDefaultLangID function (winnls.h)
description: Returns the language identifier for the system locale.
helpviewer_keywords: ["GetSystemDefaultLangID","GetSystemDefaultLangID function [Internationalization for Windows Applications]","_win32_GetSystemDefaultLangID","intl.getsystemdefaultlangid","winnls/GetSystemDefaultLangID"]
old-location: intl\getsystemdefaultlangid.htm
tech.root: Intl
ms.assetid: cf9d2f64-a8ad-46f8-9e91-a927b6b3ce08
ms.date: 12/05/2018
ms.keywords: GetSystemDefaultLangID, GetSystemDefaultLangID function [Internationalization for Windows Applications], _win32_GetSystemDefaultLangID, intl.getsystemdefaultlangid, winnls/GetSystemDefaultLangID
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
 - GetSystemDefaultLangID
 - winnls/GetSystemDefaultLangID
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
 - GetSystemDefaultLangID
---

# GetSystemDefaultLangID function


## -description

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the system locale.



## -returns

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the system locale. This is  the language used when displaying text in programs that do not support Unicode. It is set by the Administrator under <b>Control Panel</b> &gt; <b>Clock, Language, and Region</b> &gt; <b>Change date, time, or number formats</b> &gt; <b>Administrative</b> tab.

For more information on language identifiers, see <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlangid">GetUserDefaultLangID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
