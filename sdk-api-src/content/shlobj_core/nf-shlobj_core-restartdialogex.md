---
UID: NF:shlobj_core.RestartDialogEx
title: RestartDialogEx function (shlobj_core.h)
description: Displays a dialog box that asks the user to restart Windows. When the user clicks the button, the function calls ExitWindowsEx to attempt to restart Windows.
helpviewer_keywords: ["EWX_FORCE","EWX_FORCEIFHUNG","EWX_LOGOFF","EWX_POWEROFF","EWX_REBOOT","EWX_SHUTDOWN","RestartDialogEx","RestartDialogEx function [Windows Shell]","_win32_RestartDialogEx","shell.RestartDialogEx","shlobj_core/RestartDialogEx"]
old-location: shell\RestartDialogEx.htm
tech.root: shell
ms.assetid: 32bc232f-6cc4-4f19-9d33-ba7ad28dfd59
ms.date: 12/05/2018
ms.keywords: EWX_FORCE, EWX_FORCEIFHUNG, EWX_LOGOFF, EWX_POWEROFF, EWX_REBOOT, EWX_SHUTDOWN, RestartDialogEx, RestartDialogEx function [Windows Shell], _win32_RestartDialogEx, shell.RestartDialogEx, shlobj_core/RestartDialogEx
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RestartDialogEx
 - shlobj_core/RestartDialogEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - ext-ms-win-shell-shell32-l1-2-2.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Shell32.dll
api_name:
 - RestartDialogEx
---

# RestartDialogEx function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Displays a dialog box that asks the user to restart Windows. When the user clicks the button, the function calls <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> to attempt to restart Windows.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.

### -param pszPrompt [in, optional]

Type: <b>PCWSTR</b>

A null-terminated string that contains the text that displays in the dialog box to prompt the user.

### -param dwReturn

Type: <b>DWORD</b>

The flags that specify the type of shutdown.


This parameter must include one of the following values.





#### EWX_LOGOFF

Shuts down all processes running in the security context of the process that called this function. Then logs the user off.



#### EWX_POWEROFF

Shuts down the system and turns off the power. The system must support the power-off feature. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>.



#### EWX_REBOOT

Shuts down the system and then restarts the system. The calling process must have the SE_SHUTDOWN_NAME privilege. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>.



#### EWX_SHUTDOWN

Shuts down the system to a point at which it is safe to turn off the power. At this point, all file buffers have been flushed to disk, and all running processes have stopped. If the system supports the power-off feature, the power is also turned off. The calling process must have the SE_SHUTDOWN_NAME privilege. For more information, see <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>.


This parameter can optionally include the following values.





#### EWX_FORCE

Forces processes to terminate. When this flag is set, the system does not send the <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> and <a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> messages. This can cause the applications to lose data. Therefore, you should only use this flag in an emergency.



#### EWX_FORCEIFHUNG

Forces processes to terminate if they do not respond to the <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> or <a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> message. This flag is ignored if EWX_FORCE is used.

### -param dwReasonCode

Type: <b>DWORD</b>

<b>Windows XP:</b>Specifies the reason for initiating the shutdown. For more information, see <a href="/windows/desktop/Shutdown/system-shutdown-reason-codes">System Shutdown Reason Codes</a>.
    
    					

<b>Windows 2000:</b> This parameter is ignored.

## -returns

Type: <b>int</b>

Returns the identifier of the button that was pressed to close the dialog box.