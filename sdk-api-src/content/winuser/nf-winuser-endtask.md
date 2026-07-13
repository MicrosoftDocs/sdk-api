---
UID: NF:winuser.EndTask
title: EndTask function (winuser.h)
description: Forcibly closes the specified window.
helpviewer_keywords: ["EndTask","EndTask function [Windows and Messages]","_win32_EndTask","_win32_endtask_cpp","winmsg.endtask","winui._win32_endtask","winuser/EndTask"]
old-location: winmsg\endtask.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\endtask.htm
ms.date: 12/05/2018
ms.keywords: EndTask, EndTask function [Windows and Messages], _win32_EndTask, _win32_endtask_cpp, winmsg.endtask, winui._win32_endtask, winuser/EndTask
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
 - EndTask
 - winuser/EndTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - EndTask
---

# EndTask function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Forcibly closes the
		specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be closed.

### -param fShutDown [in]

Type: <b>BOOL</b>

Ignored. Must be <b>FALSE</b>.

### -param fForce [in]

Type: <b>BOOL</b>

A <b>TRUE</b> for this parameter will force the destruction of the
        window if an initial attempt fails to gently close the window using <a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a>.
        With a <b>FALSE</b> for this parameter, only the close with <b>WM_CLOSE</b> is attempted.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is <b>FALSE</b>.
				To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closewindow">CloseWindow</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-close">WM_CLOSE</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>