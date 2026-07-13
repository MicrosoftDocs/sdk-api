---
UID: NF:winbase.lstrlenW
title: lstrlenW function (winbase.h)
description: Determines the length of the specified string (not including the terminating null character). (Unicode)
helpviewer_keywords: ["_win32_lstrlen", "_win32_lstrlen_cpp", "lstrlen", "lstrlen function [Menus and Other Resources]", "lstrlenW", "menurc.lstrlen", "winbase/lstrlen", "winbase/lstrlenW", "winui._win32_lstrlen"]
old-location: menurc\lstrlen.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrlen.htm
ms.date: 12/05/2018
ms.keywords: _win32_lstrlen, _win32_lstrlen_cpp, lstrlen, lstrlen function [Menus and Other Resources], lstrlenA, lstrlenW, menurc.lstrlen, winbase/lstrlen, winbase/lstrlenA, winbase/lstrlenW, winui._win32_lstrlen
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrlenW (Unicode) and lstrlenA (ANSI)
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
 - lstrlenW
 - winbase/lstrlenW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-String-Obsolete-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - lstrlen
 - lstrlenA
 - lstrlenW
---

# lstrlenW function


## -description

Determines the length of the specified string (not including the terminating null character).

## -parameters

### -param lpString [in]

Type: <b>LPCTSTR</b>

The null-terminated string to be checked.

## -returns

Type: <b>int</b>

The function returns the length of the string, in characters. If <i>lpString</i> is <b>NULL</b>, the function returns 0.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcblengtha">StringCbLength</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchlengtha">StringCchLength</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcata">lstrcat</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpa">lstrcmp</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcpya">lstrcpy</a>

## -remarks

> [!NOTE]
> The winbase.h header defines lstrlen as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
