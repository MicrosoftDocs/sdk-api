---
UID: NF:winuser.SetClassWord
title: SetClassWord function (winuser.h)
description: Replaces the 16-bit (WORD) value at the specified offset into the extra class memory for the window class to which the specified window belongs.
helpviewer_keywords: ["SetClassWord","SetClassWord function [Windows and Messages]","_win32_SetClassWord","_win32_setclassword_cpp","winmsg.setclassword","winui._win32_setclassword","winuser/SetClassWord"]
old-location: winmsg\setclassword.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setclassword.htm
ms.date: 12/05/2018
ms.keywords: SetClassWord, SetClassWord function [Windows and Messages], _win32_SetClassWord, _win32_setclassword_cpp, winmsg.setclassword, winui._win32_setclassword, winuser/SetClassWord
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
 - SetClassWord
 - winuser/SetClassWord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
 - User32.dll
api_name:
 - SetClassWord
---

# SetClassWord function


## -description

Replaces the 16-bit (<b>WORD</b>) value at the specified offset into the extra class memory for the window class to which the specified window belongs.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga">SetClassLong</a> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.

### -param nIndex [in]

Type: <b>int</b>

The zero-based byte offset of the value to be replaced. Valid values are in the range zero through the number of bytes of class memory minus two; for example, if you specified 10 or more bytes of extra class memory, a value of 8 would be an index to the fifth 16-bit integer.

### -param wNewWord [in]

Type: <b>WORD</b>

The replacement value.

## -returns

Type: <b>WORD</b>

If the function succeeds, the return value is the previous value of the specified 16-bit integer. If the value was not previously set, the return value is zero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Reserve extra class memory by specifying a nonzero value in the 
				<b>cbClsExtra</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassword">GetClassWord</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga">SetClassLong</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>