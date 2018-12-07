---
UID: NF:winuser.CallWindowProcA
title: CallWindowProcA function
author: windows-sdk-content
description: Passes message information to the specified window procedure.
old-location: winmsg\callwindowproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowprocedures\windowprocedurereference\windowprocedurefunctions\callwindowproc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CallWindowProc, CallWindowProc function [Windows and Messages], CallWindowProcA, CallWindowProcW, _win32_CallWindowProc, _win32_callwindowproc_cpp, winmsg.callwindowproc, winui._win32_callwindowproc, winuser/CallWindowProc, winuser/CallWindowProcA, winuser/CallWindowProcW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - CallWindowProc
 - CallWindowProcA
 - CallWindowProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CallWindowProcA function


## -description


Passes message information to the specified window procedure.


## -parameters




### -param lpPrevWndFunc [in]

Type: <b>WNDPROC</b>

The previous window procedure. If this value is obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/ms633584(v=VS.85).aspx">GetWindowLong</a> function with the <i>nIndex</i> parameter set to <b>GWL_WNDPROC</b> or <b>DWL_DLGPROC</b>, it is actually either the address of a window or dialog box procedure, or a special internal value meaningful only to <b>CallWindowProc</b>. 


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



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value specifies the result of the message processing and depends on the message sent. 




## -remarks



Use the <b>CallWindowProc</b> function for window subclassing. Usually, all windows with the same class share one window procedure. A subclass is a window or set of windows with the same class whose messages are intercepted and processed by another window procedure (or procedures) before being passed to the window procedure of the class. 

The <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> function creates the subclass by changing the window procedure associated with a particular window, causing the system to call the new window procedure instead of the previous one. An application must pass any messages not processed by the new window procedure to the previous window procedure by calling <b>CallWindowProc</b>. This allows the application to create a chain of window procedures. 

If <b>STRICT</b> is defined, the <i>lpPrevWndFunc</i> parameter has the data type <b>WNDPROC</b>. The <b>WNDPROC</b> type is declared as follows:

<pre class="syntax" xml:space="preserve"><code>LRESULT (CALLBACK* WNDPROC) (HWND, UINT, WPARAM, LPARAM); </code></pre>
If <b>STRICT</b> is not defined, the <i>lpPrevWndFunc</i> parameter has the data type <b>FARPROC</b>. The <b>FARPROC</b> type is declared as follows:

<pre class="syntax" xml:space="preserve"><code>int (FAR WINAPI * FARPROC) () </code></pre>
In C, the <b>FARPROC</b> declaration indicates a callback function that has an unspecified parameter list. In C++, however, the empty parameter list in the declaration indicates that a function has no parameters. This subtle distinction can break careless code. Following is one way to handle this situation:

<pre class="syntax" xml:space="preserve"><code>#ifdef STRICT 
  WNDPROC MyWindowProcedure 
#else 
  FARPROC MyWindowProcedure 
#endif 
... 
  lResult = CallWindowProc(MyWindowProcedure, ...) ; </code></pre>
For further information about functions declared with empty argument lists, refer to 
				<i>The C++ Programming Language, Second Edition,</i> by Bjarne Stroustrup. 

The <b>CallWindowProc</b> function handles Unicode-to-ANSI conversion. You cannot take advantage of this conversion if you call the window procedure directly. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms633570(v=VS.85).aspx">Subclassing a Window</a>

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633584(v=VS.85).aspx">GetWindowLong</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633588(v=VS.85).aspx">SetClassLong</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632593(v=VS.85).aspx">Window Procedures</a>
 

 

