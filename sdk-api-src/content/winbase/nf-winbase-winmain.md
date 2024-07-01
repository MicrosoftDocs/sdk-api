---
UID: NF:winbase.WinMain
title: WinMain function (winbase.h)
description: The user-provided entry point for a graphical Windows-based application.
helpviewer_keywords: ["WinMain","WinMain callback","WinMain callback function [Windows and Messages]","_win32_WinMain","_win32_winmain_cpp","winbase/WinMain","winmsg.winmain","winui._win32_winmain"]
old-location: winmsg\winmain.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\winmain.htm
ms.date: 12/05/2018
ms.keywords: WinMain, WinMain callback, WinMain callback function [Windows and Messages], _win32_WinMain, _win32_winmain_cpp, winbase/WinMain, winmsg.winmain, winui._win32_winmain
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - WinMain
 - winbase/WinMain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbase.h
api_name:
 - WinMain
---

# WinMain function


## -description

The user-provided entry point for a graphical Windows-based application.

<b>WinMain</b> is the conventional name used for the application entry point. For more information, see Remarks.

## -parameters

### -param hInstance [in]

Type: <b>HINSTANCE</b>

A handle to the current instance of the application.

### -param hPrevInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the previous instance of the application. This parameter is always <b>NULL</b>. If you need to detect whether another instance already exists, create a uniquely named mutex using the <a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> function. <b>CreateMutex</b> will succeed even if the mutex already exists, but the  function will return <b>ERROR_ALREADY_EXISTS</b>. This indicates that another instance of your application exists, because it created the mutex first. However, a malicious user can create this mutex before you do and prevent your application from starting. To prevent this situation, create a randomly named mutex and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your application to one instance per user, create a locked file in the user's profile directory.

### -param lpCmdLine [in]

Type: <b>LPSTR</b>

The command line for the application, excluding the program name. To retrieve the entire command line, use the <a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a> function.

### -param nShowCmd [in]

Type: <b>int</b>

Controls how the window is to be shown. This parameter can be any of the values that can be specified in the <i>nCmdShow</i> parameter for the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function.

## -returns

Type: <b>int</b>

If the function succeeds, terminating when it receives a <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message, it should return the exit value contained in that message's <i>wParam</i> parameter. If the function terminates before entering the message loop, it should return zero.

## -remarks

The name <b>WinMain</b> is used by convention by many programming frameworks. Depending on the programming framework, the call to the <b>WinMain</b> function can be preceded and followed by additional activities specific to that framework.

Your <b>WinMain</b> should initialize the application, display its main window, and enter a message retrieval-and-dispatch loop that is the top-level control structure for the remainder of the application's execution. Terminate the message loop when it receives a <a href="/windows/desktop/winmsg/wm-quit">WM_QUIT</a> message. At that point, your <b>WinMain</b> should exit the application, returning the value passed in the <b>WM_QUIT</b> message's <i>wParam</i> parameter. If <b>WM_QUIT</b> was received as a result of calling <a href="/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a>, the value of <i>wParam</i> is the value of the <b>PostQuitMessage</b> function's <i>nExitCode</i> parameter. For more information, see <a href="/windows/desktop/winmsg/using-messages-and-message-queues">Creating a Message Loop</a>.

ANSI applications can use the <i>lpCmdLine</i> parameter of the <b>WinMain</b> function to access the command-line string, excluding the program name. Note that <i>lpCmdLine</i> uses the <b>LPSTR</b> data type instead of the <b>LPTSTR</b> data type. This means that <b>WinMain</b> cannot be used by Unicode programs. The <a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinew">GetCommandLineW</a> function can be used to obtain the command line as a Unicode string. Some programming frameworks might provide an alternative entry point that provides a Unicode command line. For example, the Microsoft Visual Studio C++ complier uses the name <b>wWinMain</b> for the Unicode entry point.

## Example

The following code example demonstrates the use of **WinMain**

```cpp
#include <windows.h>

int APIENTRY WinMain(HINSTANCE hInst, HINSTANCE hInstPrev, PSTR cmdline, int cmdshow)
{
    return MessageBox(NULL, "hello, world", "caption", 0);
}
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a>



<a href="/windows/desktop/api/winuser/nf-winuser-dispatchmessage">DispatchMessage</a>



<a href="/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/winuser/nf-winuser-postquitmessage">PostQuitMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
