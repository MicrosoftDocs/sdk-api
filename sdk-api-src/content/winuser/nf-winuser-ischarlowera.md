---
UID: NF:winuser.IsCharLowerA
title: IsCharLowerA function (winuser.h)
description: Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.
helpviewer_keywords: ["IsCharLowerA", "winuser/IsCharLowerA"]
old-location: menurc\ischarlower.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\ischarlower.htm
ms.date: 12/05/2018
ms.keywords: IsCharLower, IsCharLower function [Menus and Other Resources], IsCharLowerA, _win32_IsCharLower, _win32_ischarlower_cpp, menurc.ischarlower, winui._win32_ischarlower, winuser/IsCharLower, winuser/IsCharLowerA
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsCharLowerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsCharLowerA
 - winuser/IsCharLowerA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
api_name:
 - IsCharLower
 - IsCharLowerA
---

# IsCharLowerA function


## -description

Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.

## -parameters

### -param ch [in]

Type: <b>TCHAR</b>

The character to be tested.

## -returns

Type: <b>BOOL</b>

If the character is lowercase, the return value is nonzero.

If the character is not lowercase, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-ischaruppera">IsCharUpper</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>

## -remarks

> [!NOTE]
> The winuser.h header defines IsCharLower as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
