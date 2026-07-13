---
UID: NF:winuser.RegisterShellHookWindow
title: RegisterShellHookWindow function (winuser.h)
description: Registers a specified Shell window to receive certain messages for events or notifications that are useful to Shell applications.
helpviewer_keywords: ["RegisterShellHookWindow","RegisterShellHookWindow function [Windows and Messages]","_win32_RegisterShellHookWindow","_win32_registershellhookwindow_cpp","winmsg.registershellhookwindow","winui._win32_registershellhookwindow","winuser/RegisterShellHookWindow"]
old-location: winmsg\registershellhookwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\registershellhookwindow.htm
ms.date: 12/05/2018
ms.keywords: RegisterShellHookWindow, RegisterShellHookWindow function [Windows and Messages], _win32_RegisterShellHookWindow, _win32_registershellhookwindow_cpp, winmsg.registershellhookwindow, winui._win32_registershellhookwindow, winuser/RegisterShellHookWindow
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
 - RegisterShellHookWindow
 - winuser/RegisterShellHookWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-iam-l1-1-2.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-shell-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - RegisterShellHookWindow
---

# RegisterShellHookWindow function


## -description

<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Registers a specified Shell window to receive certain messages for events or notifications that are useful to Shell applications.

The event messages received are only those sent to the Shell window associated with the specified window's desktop. Many of the messages    are the same as those that can be received after calling the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a> function and specifying <b>WH_SHELL</b> for the hook type. The difference with <b>RegisterShellHookWindow</b> is that the messages are received through the specified window's <a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a> and not through a call back procedure.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to register for Shell hook messages.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.

## -remarks

As with normal window messages, the second parameter of the window procedure identifies the message as a <b>WM_SHELLHOOKMESSAGE</b>. However, for these Shell hook messages, the message value is not a pre-defined constant like other message IDs such as <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>. The value must be obtained dynamically using a call to <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> as shown here:

                

<code>RegisterWindowMessage(TEXT("SHELLHOOK"));</code>

This precludes handling these messages using a traditional switch statement which requires  ID values that are known at compile time.  For handling Shell hook messages, the normal practice is to code an If statement in the default section of your switch statement and then handle the message if the value of the message ID is the same as the value
obtained from the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> call.

The following table describes the <i>wParam</i> and <i>lParam</i> parameter values passed to the window procedure for the Shell hook messages.

<table class="clsStd">
<tr>
<th>wParam</th>
<th>lParam</th>
</tr>
<tr>
<td><b>HSHELL_GETMINRECT</b></td>
<td>A pointer to a <b>SHELLHOOKINFO</b> structure.</td>
</tr>
<tr>
<td><b>HSHELL_WINDOWACTIVATED</b></td>
<td>A handle to the activated window.</td>
</tr>
<tr>
<td><b>HSHELL_RUDEAPPACTIVATED</b></td>
<td>A handle to the activated window.</td>
</tr>
<tr>
<td><b>HSHELL_WINDOWREPLACING</b></td>
<td>A handle to the window replacing the top-level window.</td>
</tr>
<tr>
<td><b>HSHELL_WINDOWREPLACED</b></td>
<td>A handle to the window being replaced.</td>
</tr>
<tr>
<td><b>HSHELL_WINDOWCREATED</b></td>
<td>A handle to the window being created.</td>
</tr>
<tr>
<td><b>HSHELL_WINDOWDESTROYED</b></td>
<td>A handle to the top-level window being destroyed.</td>
</tr>
<tr>
<td><b>HSHELL_ACTIVATESHELLWINDOW</b></td>
<td>Not used.</td>
</tr>
<tr>
<td><b>HSHELL_TASKMAN</b></td>
<td>Can be ignored.</td>
</tr>
<tr>
<td><b>HSHELL_REDRAW</b></td>
<td>A handle to the window that needs to be redrawn.</td>
</tr>
<tr>
<td><b>HSHELL_FLASH</b></td>
<td>A handle to the window that needs to be flashed.</td>
</tr>
<tr>
<td><b>HSHELL_ENDTASK</b></td>
<td>A handle to the window that should be forced to exit.</td>
</tr>
<tr>
<td><b>HSHELL_APPCOMMAND</b></td>
<td>The APPCOMMAND which has been unhandled by the application or other hooks. See <a href="/windows/desktop/inputdev/wm-appcommand">WM_APPCOMMAND</a> and use the <a href="/windows/desktop/api/winuser/nf-winuser-get_appcommand_lparam">GET_APPCOMMAND_LPARAM</a> macro to retrieve this parameter.</td>
</tr>
<tr>
<td><b>HSHELL_MONITORCHANGED                     </b></td>
<td>A handle to the window that moved to a different monitor.</td>
</tr>
</table>
 

This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-deregistershellhookwindow">DeregisterShellHookWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>



<a href="/windows/win32/winmsg/shellproc">ShellProc</a>



<a href="/windows/desktop/winmsg/using-messages-and-message-queues">Using Messages and Message Queues</a>



<a href="/windows/desktop/WinAuto/winevents-infrastructure">WinEvents</a>



<a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>