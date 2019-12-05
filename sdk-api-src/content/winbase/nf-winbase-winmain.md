---
UID: NF:winbase.WinMain
title: WinMain function (winbase.h)
description: The user-provided entry point for a graphical Windows-based application.
old-location: winmsg\winmain.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\winmain.htm
ms.date: 12/05/2018
ms.keywords: SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, WinMain, WinMain callback, WinMain callback function [Windows and Messages], _win32_WinMain, _win32_winmain_cpp, winbase/WinMain, winmsg.winmain, winui._win32_winmain
ms.topic: function
f1_keywords:
- winbase/WinMain
dev_langs:
- c++
req.header: winbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbase.h
api_name:
- WinMain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WinMain function


## -description


The user-provided entry point for a graphical Windows-based application.

<b>WinMain</b> is the conventional name used for the application entry point. For more information, see Remarks.


## -parameters




### -param hInstance [in]

Type: <b>HINSTANCE</b>

A handle to the current instance of the application.


### -param hPrevInstance [in]

Type: <b>HINSTANCE</b>

A handle to the previous instance of the application. This parameter is always <b>NULL</b>. If you need to detect whether another instance already exists, create a uniquely named mutex using the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> function. <b>CreateMutex</b> will succeed even if the mutex already exists, but the  function will return <b>ERROR_ALREADY_EXISTS</b>. This indicates that another instance of your application exists, because it created the mutex first. However, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.


### -param lpCmdLine [in]

Type: <b>LPSTR</b>

The command line for the application, excluding the program name. To retrieve the entire command line, use the <a href="https://docs.microsoft.com/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a> function.


### -param nShowCmd

TBD




#### - nCmdShow [in]

Type: <b>int</b>

Controls how the window is to be shown. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_HIDE"></a><a id="sw_hide"></a><dl>
<dt><b>SW_HIDE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Hides the window and activates another window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_MAXIMIZE"></a><a id="sw_maximize"></a><dl>
<dt><b>SW_MAXIMIZE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Maximizes the specified window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_MINIMIZE"></a><a id="sw_minimize"></a><dl>
<dt><b>SW_MINIMIZE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Minimizes the specified window and activates the next top-level window in the Z order.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_RESTORE"></a><a id="sw_restore"></a><dl>
<dt><b>SW_RESTORE</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Activates and displays the window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when restoring a minimized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOW"></a><a id="sw_show"></a><dl>
<dt><b>SW_SHOW</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it in its current size and position.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMAXIMIZED"></a><a id="sw_showmaximized"></a><dl>
<dt><b>SW_SHOWMAXIMIZED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it as a maximized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMINIMIZED"></a><a id="sw_showminimized"></a><dl>
<dt><b>SW_SHOWMINIMIZED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Activates the window and displays it as a minimized window.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWMINNOACTIVE"></a><a id="sw_showminnoactive"></a><dl>
<dt><b>SW_SHOWMINNOACTIVE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Displays the window as a minimized window. This value is similar to <b>SW_SHOWMINIMIZED</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNA"></a><a id="sw_showna"></a><dl>
<dt><b>SW_SHOWNA</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Displays the window in its current size and position. This value is similar to <b>SW_SHOW</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNOACTIVATE"></a><a id="sw_shownoactivate"></a><dl>
<dt><b>SW_SHOWNOACTIVATE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Displays a window in its most recent size and position. This value is similar to <b>SW_SHOWNORMAL</b>, except the window is not activated.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SHOWNORMAL"></a><a id="sw_shownormal"></a><dl>
<dt><b>SW_SHOWNORMAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Activates and displays a window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>int</b>
</strong>

If the function succeeds, terminating when it receives a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message, it should return the exit value contained in that message's <i>wParam</i> parameter. If the function terminates before entering the message loop, it should return zero.




## -remarks



The name <b>WinMain</b> is used by convention by many programming frameworks. Depending on the programming framework, the call to the <b>WinMain</b> function can be preceded and followed by additional activities specific to that framework.

Your <b>WinMain</b> should initialize the application, display its main window, and enter a message retrieval-and-dispatch loop that is the top-level control structure for the remainder of the application's execution. Terminate the message loop when it receives a <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message. At that point, your <b>WinMain</b> should exit the application, returning the value passed in the <b>WM_QUIT</b> message's <i>wParam</i> parameter. If <b>WM_QUIT</b> was received as a result of calling <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a>, the value of <i>wParam</i> is the value of the <b>PostQuitMessage</b> function's <i>nExitCode</i> parameter. For more information, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/using-messages-and-message-queues">Creating a Message Loop</a>.

ANSI applications can use the <i>lpCmdLine</i> parameter of the <b>WinMain</b> function to access the command-line string, excluding the program name. Note that <i>lpCmdLine</i> uses the <b>LPSTR</b> data type instead of the <b>LPTSTR</b> data type. This means that <b>WinMain</b> cannot be used by Unicode programs. The <a href="https://docs.microsoft.com/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLineW</a> function can be used to obtain the command line as a Unicode string. Some programming frameworks might provide an alternative entry point that provides a Unicode command line. For example, the Microsoft Visual Studio C++ complier uses the name <b>wWinMain</b> for the Unicode entry point.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

