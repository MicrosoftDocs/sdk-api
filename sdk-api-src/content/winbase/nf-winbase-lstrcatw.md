---
UID: NF:winbase.lstrcatW
title: lstrcatW function (winbase.h)
description: Appends one string to another.Warning  Do not use. (Unicode)
helpviewer_keywords: ["_win32_lstrcat", "_win32_lstrcat_cpp", "lstrcat", "lstrcat function [Menus and Other Resources]", "lstrcatW", "menurc.lstrcat", "winbase/lstrcat", "winbase/lstrcatW", "winui._win32_lstrcat"]
old-location: menurc\lstrcat.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\lstrcat.htm
ms.date: 12/05/2018
ms.keywords: _win32_lstrcat, _win32_lstrcat_cpp, lstrcat, lstrcat function [Menus and Other Resources], lstrcatA, lstrcatW, menurc.lstrcat, winbase/lstrcat, winbase/lstrcatA, winbase/lstrcatW, winui._win32_lstrcat
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lstrcatW (Unicode) and lstrcatA (ANSI)
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
 - lstrcatW
 - winbase/lstrcatW
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
api_name:
 - lstrcat
 - lstrcatA
 - lstrcatW
---

# lstrcatW function


## -description

Appends one string to another.
<div class="alert"><b>Warning</b>  Do not use. Consider using <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcata">StringCchCat</a> instead. See Security Considerations. </div><div> </div>

## -parameters

### -param lpString1 [in, out]

Type: <b>LPTSTR</b>

The first null-terminated string. This buffer must be large enough 
				to contain both strings.

### -param lpString2 [in]

Type: <b>LPTSTR</b>

The null-terminated string to be appended to the string 
				specified in the <i>lpString1</i> parameter.

## -returns

Type: <b>LPTSTR</b>

If the function succeeds, the return value is a pointer to the buffer.

If the function fails, the return value is <b>NULL</b> 
                    and <i>lpString1</i> may not be null-terminated.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcata">StringCbCat</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatnexa">StringCbCatNEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcata">StringCchCat</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatexa">StringCchCatEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatna">StringCchCatN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatnexa">StringCchCatNEx</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpa">lstrcmp</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrcmpia">lstrcmpi</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lstrlena">lstrlen</a>

## -remarks

> [!NOTE]
> The winbase.h header defines lstrcat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
