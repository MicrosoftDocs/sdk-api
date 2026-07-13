---
UID: NF:winuser.DestroyCaret
title: DestroyCaret function (winuser.h)
description: Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.
helpviewer_keywords: ["DestroyCaret","DestroyCaret function [Menus and Other Resources]","_win32_DestroyCaret","_win32_destroycaret_cpp","menurc.destroycaret","winui._win32_destroycaret","winuser/DestroyCaret"]
old-location: menurc\destroycaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\destroycaret.htm
ms.date: 12/05/2018
ms.keywords: DestroyCaret, DestroyCaret function [Menus and Other Resources], _win32_DestroyCaret, _win32_destroycaret_cpp, menurc.destroycaret, winui._win32_destroycaret, winuser/DestroyCaret
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
 - DestroyCaret
 - winuser/DestroyCaret
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
 - DestroyCaret
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# DestroyCaret function


## -description

Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>DestroyCaret</b> destroys the caret only if a window in the current task owns the caret. If a window that is not in the current task owns the caret, <b>DestroyCaret</b> does nothing and returns <b>FALSE</b>. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 

For an example, see <a href="/windows/desktop/menurc/using-carets">Destroying a Caret</a>

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createcaret">CreateCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-hidecaret">HideCaret</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a>
