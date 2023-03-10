---
UID: NF:winuser.HideCaret
title: HideCaret function (winuser.h)
description: Removes the caret from the screen. Hiding a caret does not destroy its current shape or invalidate the insertion point.
helpviewer_keywords: ["HideCaret","HideCaret function [Menus and Other Resources]","_win32_HideCaret","_win32_hidecaret_cpp","menurc.hidecaret","winui._win32_hidecaret","winuser/HideCaret"]
old-location: menurc\hidecaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\hidecaret.htm
ms.date: 12/05/2018
ms.keywords: HideCaret, HideCaret function [Menus and Other Resources], _win32_HideCaret, _win32_hidecaret_cpp, menurc.hidecaret, winui._win32_hidecaret, winuser/HideCaret
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
 - HideCaret
 - winuser/HideCaret
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
 - HideCaret
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# HideCaret function


## -description

Removes the caret from the screen. Hiding a caret does not destroy its current shape or invalidate the insertion point.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the caret. If this parameter is <b>NULL</b>, <b>HideCaret</b> searches the current task for the window that owns the caret.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>HideCaret</b> hides the caret only if the specified window owns the caret. If the specified window does not own the caret, <b>HideCaret</b> does nothing and returns <b>FALSE</b>. 

Hiding is cumulative. If your application calls <b>HideCaret</b> five times in a row, it must also call <a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a> five times before the caret is displayed. 

For an example, see <a href="/windows/desktop/menurc/using-carets">Hiding a Caret</a>.

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createcaret">CreateCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroycaret">DestroyCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcaretpos">GetCaretPos</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a>
