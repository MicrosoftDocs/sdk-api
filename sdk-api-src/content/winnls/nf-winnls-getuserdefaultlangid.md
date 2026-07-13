---
UID: NF:winnls.GetUserDefaultLangID
title: GetUserDefaultLangID function (winnls.h)
description: Returns the language identifier of the Region Format setting for the current user.
helpviewer_keywords: ["GetUserDefaultLangID","GetUserDefaultLangID function [Internationalization for Windows Applications]","_win32_GetUserDefaultLangID","intl.getuserdefaultlangid","winnls/GetUserDefaultLangID"]
old-location: intl\getuserdefaultlangid.htm
tech.root: Intl
ms.assetid: b1f25fc1-9435-4e9b-b8d0-a670a198ab3a
ms.date: 12/05/2018
ms.keywords: GetUserDefaultLangID, GetUserDefaultLangID function [Internationalization for Windows Applications], _win32_GetUserDefaultLangID, intl.getuserdefaultlangid, winnls/GetUserDefaultLangID
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
 - GetUserDefaultLangID
 - winnls/GetUserDefaultLangID
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
 - GetUserDefaultLangID
---

# GetUserDefaultLangID function


## -description

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> of the Region Format setting for the current user.



## -returns

Returns the <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the current user as set under <b>Control Panel</b> &gt; <b>Clock, Language, and Region</b> &gt; <b>Change date, time, or number formats</b> &gt; <b>Formats</b> tab &gt; <b>Format</b> dropdown.

For more information on language identifiers, see <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

## -remarks

The return value is not necessarily the same as that returned by <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlangid">GetSystemDefaultLangID</a>, even for a single-user computer.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlangid">GetSystemDefaultLangID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
