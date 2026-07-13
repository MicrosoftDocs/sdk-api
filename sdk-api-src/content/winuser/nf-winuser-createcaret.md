---
UID: NF:winuser.CreateCaret
title: CreateCaret function (winuser.h)
description: Creates a new shape for the system caret and assigns ownership of the caret to the specified window. The caret shape can be a line, a block, or a bitmap.
helpviewer_keywords: ["CreateCaret","CreateCaret function [Menus and Other Resources]","_win32_CreateCaret","_win32_createcaret_cpp","menurc.createcaret","winui._win32_createcaret","winuser/CreateCaret"]
old-location: menurc\createcaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\createcaret.htm
ms.date: 12/05/2018
ms.keywords: CreateCaret, CreateCaret function [Menus and Other Resources], _win32_CreateCaret, _win32_createcaret_cpp, menurc.createcaret, winui._win32_createcaret, winuser/CreateCaret
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
 - CreateCaret
 - winuser/CreateCaret
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
 - CreateCaret
req.apiset: ext-ms-win-ntuser-caret-l1-1-0 (introduced in Windows 8)
---

# CreateCaret function


## -description

Creates a new shape for the system caret and assigns ownership of the caret to the specified window. The caret shape can be a line, a block, or a bitmap.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that owns the caret.

### -param hBitmap [in, optional]

Type: <b>HBITMAP</b>

A handle to the bitmap that defines the caret shape. If this parameter is <b>NULL</b>, the caret is solid. If this parameter is <code>(HBITMAP) 1</code>, the caret is gray. If this parameter is a bitmap handle, the caret is the specified bitmap. The bitmap handle must have been created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a> function.
The caret is drawn to the screen via the XOR operation.

If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores the <i>nWidth</i> and <i>nHeight</i> parameters; the bitmap defines its own width and height.
The application should not delete the <i>hBitmap</i> until the caret is destroyed or replaced by another caret.

### -param nWidth [in]

Type: <b>int</b>

The width of the caret, in logical units. If this parameter is zero, the width is set to the system-defined window border width. If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores this parameter.

### -param nHeight [in]

Type: <b>int</b>

The height of the caret, in logical units. If this parameter is zero, the height is set to the system-defined window border height. If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores this parameter.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.
                    

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <i>nWidth</i> and <i>nHeight</i> parameters specify the caret's width and height, in logical units; the exact width and height, in pixels, depend on the window's mapping mode. 

<b>CreateCaret</b> automatically destroys the previous caret shape, if any, regardless of the window that owns the caret. The caret is hidden until the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a> function to make the caret visible. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The width and height parameters are interpreted as logical sizes in terms of the window in question. The calling thread is not taken into consideration.

## -see-also

<a href="/windows/desktop/menurc/carets">Carets</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroycaret">DestroyCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/api/winuser/nf-winuser-hidecaret">HideCaret</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showcaret">ShowCaret</a>
