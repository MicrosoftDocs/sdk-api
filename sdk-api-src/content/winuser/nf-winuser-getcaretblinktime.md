---
UID: NF:winuser.GetCaretBlinkTime
title: GetCaretBlinkTime function (winuser.h)
description: Retrieves the time required to invert the caret's pixels. The user can set this value.
helpviewer_keywords: ["GetCaretBlinkTime","GetCaretBlinkTime function [Menus and Other Resources]","_win32_GetCaretBlinkTime","_win32_getcaretblinktime_cpp","menurc.getcaretblinktime","winui._win32_getcaretblinktime","winuser/GetCaretBlinkTime"]
old-location: menurc\getcaretblinktime.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\getcaretblinktime.htm
ms.date: 12/05/2018
ms.keywords: GetCaretBlinkTime, GetCaretBlinkTime function [Menus and Other Resources], _win32_GetCaretBlinkTime, _win32_getcaretblinktime_cpp, menurc.getcaretblinktime, winui._win32_getcaretblinktime, winuser/GetCaretBlinkTime
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCaretBlinkTime
 - winuser/GetCaretBlinkTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - GetCaretBlinkTime
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# GetCaretBlinkTime function


## -description

Retrieves the time required to invert the caret's pixels.
          The user can set this value.



## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is the blink time, in milliseconds.
          

A return value of <b>INFINITE</b> indicates that the caret does not blink.

A return value is zero indicates that the function has failed.
             To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretblinktime">SetCaretBlinkTime</a>
