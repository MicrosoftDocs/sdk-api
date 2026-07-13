---
UID: NF:winuser.CallWindowProcW
title: CallWindowProcW function (winuser.h)
description: Passes message information to the specified window procedure. (Unicode)
helpviewer_keywords: ["CallWindowProc", "CallWindowProc function [Windows and Messages]", "CallWindowProcW", "_win32_CallWindowProc", "_win32_callwindowproc_cpp", "winmsg.callwindowproc", "winui._win32_callwindowproc", "winuser/CallWindowProc", "winuser/CallWindowProcW"]
old-location: winmsg\callwindowproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowprocedures\windowprocedurereference\windowprocedurefunctions\callwindowproc.htm
ms.date: 12/05/2018
ms.keywords: CallWindowProc, CallWindowProc function [Windows and Messages], CallWindowProcA, CallWindowProcW, _win32_CallWindowProc, _win32_callwindowproc_cpp, winmsg.callwindowproc, winui._win32_callwindowproc, winuser/CallWindowProc, winuser/CallWindowProcA, winuser/CallWindowProcW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CallWindowProcW (Unicode) and CallWindowProcA (ANSI)
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
 - CallWindowProcW
 - winuser/CallWindowProcW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - CallWindowProc
 - CallWindowProcA
 - CallWindowProcW
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# CallWindowProcW function


## -description

Passes message information to the specified window procedure.

## -parameters

### -param lpPrevWndFunc [in]

Type: <b>WNDPROC</b>

The previous window procedure. If this value is obtained by calling the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a> function with the <i>nIndex</i> parameter set to <b>GWL_WNDPROC</b> or <b>DWL_DLGPROC</b>, it is actually either the address of a window or dialog box procedure, or a special internal value meaningful only to <b>CallWindowProc</b>.

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window procedure to receive the message.

### -param Msg [in]

Type: <b>UINT</b>

The message.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information. The contents of this parameter depend on the value of the <i>Msg</i> parameter.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information. The contents of this parameter depend on the value of the <i>Msg</i> parameter.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the message processing and depends on the message sent.

## -remarks

Use the <b>CallWindowProc</b> function for window subclassing. Usually, all windows with the same class share one window procedure. A subclass is a window or set of windows with the same class whose messages are intercepted and processed by another window procedure (or procedures) before being passed to the window procedure of the class. 

The <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> function creates the subclass by changing the window procedure associated with a particular window, causing the system to call the new window procedure instead of the previous one. An application must pass any messages not processed by the new window procedure to the previous window procedure by calling <b>CallWindowProc</b>. This allows the application to create a chain of window procedures. 

If <b>STRICT</b> is defined, the <i>lpPrevWndFunc</i> parameter has the data type <b>WNDPROC</b>. The <b>WNDPROC</b> type is declared as follows:


``` syntax
LRESULT (CALLBACK* WNDPROC) (HWND, UINT, WPARAM, LPARAM); 
```

If <b>STRICT</b> is not defined, the <i>lpPrevWndFunc</i> parameter has the data type <b>FARPROC</b>. The <b>FARPROC</b> type is declared as follows:


``` syntax
int (FAR WINAPI * FARPROC) () 
```

In C, the <b>FARPROC</b> declaration indicates a callback function that has an unspecified parameter list. In C++, however, the empty parameter list in the declaration indicates that a function has no parameters. This subtle distinction can break careless code. Following is one way to handle this situation:


``` syntax
#ifdef STRICT 
  WNDPROC MyWindowProcedure 
#else 
  FARPROC MyWindowProcedure 
#endif 
... 
  lResult = CallWindowProc(MyWindowProcedure, ...) ; 
```

For further information about functions declared with empty argument lists, refer to 
				<i>The C++ Programming Language, Second Edition,</i> by Bjarne Stroustrup. 

The <b>CallWindowProc</b> function handles Unicode-to-ANSI conversion. You cannot take advantage of this conversion if you call the window procedure directly. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-procedures">Subclassing a Window</a>

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines CallWindowProc as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowlonga">GetWindowLong</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga">SetClassLong</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a>



<a href="/windows/desktop/winmsg/window-procedures">Window Procedures</a>
