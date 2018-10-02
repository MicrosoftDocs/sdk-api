---
UID: NF:shlobj_core.RestartDialog
title: RestartDialog function
author: windows-sdk-content
description: Displays a dialog box that prompts the user to restart Windows. When the user clicks the button, the function calls ExitWindowsEx to attempt to restart Windows.
old-location: shell\RestartDialog.htm
tech.root: Shell
ms.assetid: ec1e3c11-9960-482c-8461-72c4d41dff3c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EWX_FORCE, EWX_FORCEIFHUNG, EWX_LOGOFF, EWX_POWEROFF, EWX_REBOOT, EWX_SHUTDOWN, RestartDialog, RestartDialog function [Windows Shell], _win32_RestartDialog, shell.RestartDialog, shlobj_core/RestartDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - RestartDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RestartDialog function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Displays a dialog box that prompts the user to restart Windows. When the user clicks the button, the function calls <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> to attempt to restart Windows.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.


### -param pszPrompt [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the text that displays in the dialog box which prompts the user.


### -param dwReturn

Type: <b>DWORD</b>

The flags that specify the type of shutdown.


This parameter must include one of the following values.





#### EWX_LOGOFF

Shuts down all processes running in the security context of the process that called this function, then logs the user off.



#### EWX_POWEROFF

Shuts down the system and turns off the power. The system must support the power-off feature. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. For more information, see <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>.



#### EWX_REBOOT

Shuts down the system and then restarts the system. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. For more information, see <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>.



#### EWX_SHUTDOWN

Shuts down the system to a point at which it is safe to turn off the power. At this point, all file buffers have been flushed to disk, and all running processes have stopped. If the system supports the power-off feature, the power is also turned off. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. For more information, see <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>.


This parameter can optionally include the following values.





#### EWX_FORCE

Forces processes to terminate. When this flag is set, the system does not send the <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> and <a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> messages. This can cause the applications to lose data. Therefore, you should only use this flag in an emergency.



#### EWX_FORCEIFHUNG

Forces processes to terminate if they do not respond to the <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> or <a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> message. This flag is ignored if <b>EWX_FORCE</b> is used.


## -returns



Type: <b>int</b>

Returns the identifier of the button that was pressed to close the dialog box.



