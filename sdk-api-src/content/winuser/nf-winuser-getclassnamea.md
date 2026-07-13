---
UID: NF:winuser.GetClassNameA
title: GetClassNameA function (winuser.h)
description: Retrieves the name of the class to which the specified window belongs. (GetClassNameA)
helpviewer_keywords: ["GetClassNameA", "winuser/GetClassNameA"]
old-location: winmsg\getclassname.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassname.htm
ms.date: 12/05/2018
ms.keywords: GetClassName, GetClassName function [Windows and Messages], GetClassNameA, GetClassNameW, _win32_GetClassName, _win32_getclassname_cpp, winmsg.getclassname, winui._win32_getclassname, winuser/GetClassName, winuser/GetClassNameA, winuser/GetClassNameW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetClassNameW (Unicode) and GetClassNameA (ANSI)
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
 - GetClassNameA
 - winuser/GetClassNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - GetClassName
 - GetClassNameA
 - GetClassNameW
req.apiset: ext-ms-win-ntuser-windowclass-l1-1-0 (introduced in Windows 8)
---

# GetClassNameA function


## -description

Retrieves the name of the class to which the specified window belongs.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param lpClassName [out]

Type: <b>LPTSTR</b>

The class name string.

### -param nMaxCount [in]

Type: <b>int</b>

The length of the *lpClassName* buffer, in characters. The buffer must be large enough to include the terminating null character; otherwise, the class name string is truncated to `nMaxCount-1` characters.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the number of 
						characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-findwindowa">FindWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa">GetClassInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga">GetClassLong</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassword">GetClassWord</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>

## -remarks

> [!NOTE]
> The winuser.h header defines GetClassName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
