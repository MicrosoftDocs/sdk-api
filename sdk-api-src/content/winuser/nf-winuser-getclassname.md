---
UID: NF:winuser.GetClassName
title: GetClassName function (winuser.h)
description: The GetClassName function retrieves the name of the class to which the specified window belongs. (GetClassName)
helpviewer_keywords: ["GetClassName","GetClassName function [Windows and Messages]","GetClassNameA","GetClassNameW","_win32_GetClassName","_win32_getclassname_cpp","winmsg.getclassname","winui._win32_getclassname","winuser/GetClassName","winuser/GetClassNameA","winuser/GetClassNameW"]
old-location: winmsg\getclassname.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclassname.htm
ms.date: 08/02/2022
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
 - GetClassName
 - winuser/GetClassName
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

# GetClassName function


## -description

Retrieves the name of the class to which the specified window belongs.

## -parameters

### -param hWnd [in]

Type: **HWND**

A handle to the window and, indirectly, the class to which the window belongs.

### -param lpClassName [out]

Type: **LPTSTR**

The class name string.

### -param nMaxCount [in]

Type: **int**

The length of the *lpClassName* buffer, in characters. The buffer must be large enough to include the terminating null character; otherwise, the class name string is truncated to `nMaxCount-1` characters.

## -returns

Type: **int**

If the function succeeds, the return value is the number of characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call [GetLastError function](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

[FindWindowA function](nf-winuser-findwindowa.md), [GetClassInfoA function](nf-winuser-getclassinfoa.md), [GetClassLongA function](nf-winuser-getclasslonga.md), [GetClassWord function](nf-winuser-getclassword.md), [Window Classes](/windows/desktop/winmsg/window-classes)
