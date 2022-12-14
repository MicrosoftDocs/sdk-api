---
UID: NF:winuser.SetCaretPos
title: SetCaretPos function (winuser.h)
description: Moves the caret to the specified coordinates. If the window that owns the caret was created with the CS_OWNDC class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.
helpviewer_keywords: ["SetCaretPos","SetCaretPos function [Menus and Other Resources]","_win32_SetCaretPos","_win32_setcaretpos_cpp","menurc.setcaretpos","winui._win32_setcaretpos","winuser/SetCaretPos"]
old-location: menurc\setcaretpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\setcaretpos.htm
ms.date: 12/05/2018
ms.keywords: SetCaretPos, SetCaretPos function [Menus and Other Resources], _win32_SetCaretPos, _win32_setcaretpos_cpp, menurc.setcaretpos, winui._win32_setcaretpos, winuser/SetCaretPos
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
 - SetCaretPos
 - winuser/SetCaretPos
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
 - SetCaretPos
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# SetCaretPos function


## -description

Moves the caret to the specified coordinates. If the window that owns the caret was created with the <b>CS_OWNDC</b> class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.

## -parameters

### -param X [in]

Type: <b>int</b>

The new x-coordinate of the caret.

### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the caret.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetCaretPos</b> moves the caret whether the caret is hidden. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. A window can set the caret position only if it owns the caret. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The provided position is interpreted as logical coordinates in terms of the window associated with the caret. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-carets">Creating and Displaying a Caret</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getcaretpos">GetCaretPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-hidecaret">HideCaret</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a>
