---
UID: NF:winuser.ShowCaret
title: ShowCaret function (winuser.h)
description: Makes the caret visible on the screen at the caret's current position. When the caret becomes visible, it begins flashing automatically.
helpviewer_keywords: ["ShowCaret","ShowCaret function [Menus and Other Resources]","_win32_ShowCaret","_win32_showcaret_cpp","menurc.showcaret","winui._win32_showcaret","winuser/ShowCaret"]
old-location: menurc\showcaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\showcaret.htm
ms.date: 12/05/2018
ms.keywords: ShowCaret, ShowCaret function [Menus and Other Resources], _win32_ShowCaret, _win32_showcaret_cpp, menurc.showcaret, winui._win32_showcaret, winuser/ShowCaret
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
 - ShowCaret
 - winuser/ShowCaret
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
 - ShowCaret
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# ShowCaret function


## -description

Makes the caret visible on the screen at the caret's current position. When the caret becomes visible, it begins flashing automatically.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the caret. If this parameter is <b>NULL</b>, <b>ShowCaret</b> searches the current task for the window that owns the caret.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>ShowCaret</b> shows the caret only if the specified window owns the caret, the caret has a shape, and the caret has not been hidden two or more times in a row. If one or more of these conditions is not met, <b>ShowCaret</b> does nothing and returns <b>FALSE</b>. 

Hiding is cumulative. If your application calls <a href="/windows/desktop/api/winuser/nf-winuser-hidecaret">HideCaret</a> five times in a row, it must also call <b>ShowCaret</b> five times before the caret reappears. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-carets">Creating and Displaying a Caret</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createcaret">CreateCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroycaret">DestroyCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcaretpos">GetCaretPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-hidecaret">HideCaret</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>
