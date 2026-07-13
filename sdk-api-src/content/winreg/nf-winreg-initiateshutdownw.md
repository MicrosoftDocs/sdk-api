---
UID: NF:winreg.InitiateShutdownW
title: InitiateShutdownW function (winreg.h)
description: Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart. (Unicode)
helpviewer_keywords: ["InitiateShutdown", "InitiateShutdown function", "InitiateShutdownW", "SHUTDOWN_FORCE_OTHERS", "SHUTDOWN_FORCE_SELF", "SHUTDOWN_GRACE_OVERRIDE", "SHUTDOWN_HYBRID", "SHUTDOWN_INSTALL_UPDATES", "SHUTDOWN_NOREBOOT", "SHUTDOWN_POWEROFF", "SHUTDOWN_RESTART", "SHUTDOWN_RESTARTAPPS", "base.initiateshutdown", "security.initiateshutdown", "winreg/InitiateShutdown", "winreg/InitiateShutdownW"]
old-location: base\initiateshutdown.htm
tech.root: base
ms.assetid: 9d0d3774-3e4d-4e56-b4c2-d59d74e797a1
ms.date: 12/05/2018
ms.keywords: InitiateShutdown, InitiateShutdown function, InitiateShutdownA, InitiateShutdownW, SHUTDOWN_FORCE_OTHERS, SHUTDOWN_FORCE_SELF, SHUTDOWN_GRACE_OVERRIDE, SHUTDOWN_HYBRID, SHUTDOWN_INSTALL_UPDATES, SHUTDOWN_NOREBOOT, SHUTDOWN_POWEROFF, SHUTDOWN_RESTART, SHUTDOWN_RESTARTAPPS, base.initiateshutdown, security.initiateshutdown, winreg/InitiateShutdown, winreg/InitiateShutdownA, winreg/InitiateShutdownW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InitiateShutdownW (Unicode) and InitiateShutdownA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitiateShutdownW
 - winreg/InitiateShutdownW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-shutdown-l1-1-1.dll
 - advapi32legacy.dll
 - Ext-MS-Win-AdvAPI32-shutdown-l1-1-0.dll
api_name:
 - InitiateShutdown
 - InitiateShutdownA
 - InitiateShutdownW
---

# InitiateShutdownW function


## -description

Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.

## -parameters

### -param lpMachineName [in, optional]

The name of the computer to be shut down. If the value of this parameter is <b>NULL</b>, the local computer is shut down.

### -param lpMessage [in, optional]

The message to be displayed in the interactive shutdown dialog box.

### -param dwGracePeriod [in]

The number of seconds to wait before shutting down the computer. If the value of this parameter is zero, the computer is shut down immediately. This value is limited to <b>MAX_SHUTDOWN_TIMEOUT</b>.

If the value of this parameter is greater than zero, and the <i>dwShutdownFlags</i> parameter specifies the flag <b>SHUTDOWN_GRACE_OVERRIDE</b>, the function fails and returns the error code <b>ERROR_BAD_ARGUMENTS</b>.

### -param dwShutdownFlags [in]

One or more bit flags that specify options for the shutdown. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_FORCE_OTHERS"></a><a id="shutdown_force_others"></a><dl>
<dt><b>SHUTDOWN_FORCE_OTHERS</b></dt>
<dt>0x00000001 (0x1)</dt>
</dl>
</td>
<td width="60%">
All sessions are forcefully logged off. If this flag is not set and users other than the current user are logged on to the computer specified by the <i>lpMachineName</i> parameter, this function fails with a return value of <b>ERROR_SHUTDOWN_USERS_LOGGED_ON</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_FORCE_SELF"></a><a id="shutdown_force_self"></a><dl>
<dt><b>SHUTDOWN_FORCE_SELF</b></dt>
<dt>0x00000002 (0x2)</dt>
</dl>
</td>
<td width="60%">
Specifies that the originating session is logged off forcefully. If this flag is not set, the originating session is shut down interactively, so a shutdown is not guaranteed even if the function returns successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_GRACE_OVERRIDE"></a><a id="shutdown_grace_override"></a><dl>
<dt><b>SHUTDOWN_GRACE_OVERRIDE</b></dt>
<dt>0x00000020 (0x20)</dt>
</dl>
</td>
<td width="60%">
Overrides the grace period so that the computer is shut down immediately.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_HYBRID"></a><a id="shutdown_hybrid"></a><dl>
<dt><b>SHUTDOWN_HYBRID</b></dt>
<dt>0x00000200 (0x200)</dt>
</dl>
</td>
<td width="60%">
Beginning with <b>InitiateShutdown</b> running on Windows 8, you must include the <b>SHUTDOWN_HYBRID</b> flag with one or more of the flags in this table to specify options for the shutdown.  

Beginning with Windows 8, <b>InitiateShutdown</b> always initiate a full system shutdown if the <b>SHUTDOWN_HYBRID</b> flag is absent.  

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_INSTALL_UPDATES"></a><a id="shutdown_install_updates"></a><dl>
<dt><b>SHUTDOWN_INSTALL_UPDATES</b></dt>
<dt>0x00000040 (0x40)</dt>
</dl>
</td>
<td width="60%">
The computer installs any updates before starting the shutdown.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_NOREBOOT"></a><a id="shutdown_noreboot"></a><dl>
<dt><b>SHUTDOWN_NOREBOOT</b></dt>
<dt>0x00000010 (0x10)</dt>
</dl>
</td>
<td width="60%">
The computer is shut down but is not powered down or rebooted.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_POWEROFF"></a><a id="shutdown_poweroff"></a><dl>
<dt><b>SHUTDOWN_POWEROFF</b></dt>
<dt>0x00000008 (0x8)</dt>
</dl>
</td>
<td width="60%">
The computer is shut down and powered down.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_RESTART"></a><a id="shutdown_restart"></a><dl>
<dt><b>SHUTDOWN_RESTART</b></dt>
<dt>0x00000004 (0x4)</dt>
</dl>
</td>
<td width="60%">
The computer is shut down and rebooted.

</td>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_RESTARTAPPS"></a><a id="shutdown_restartapps"></a><dl>
<dt><b>SHUTDOWN_RESTARTAPPS</b></dt>
<dt>0x00000080 (0x80)</dt>
</dl>
</td>
<td width="60%">
The system is rebooted using the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function with the EWX_RESTARTAPPS flag. This restarts any applications that have been registered for restart using the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function.

</td>
</tr>
</table>

### -param dwReason [in]

The reason for initiating the shutdown. This parameter must be one of the <a href="/windows/desktop/Shutdown/system-shutdown-reason-codes">system shutdown reason codes</a>. 
If this parameter is zero, the default is an undefined shutdown that is logged as "No title for this reason could be found". By default, it is also an unplanned shutdown. Depending on how the system is configured, an unplanned shutdown triggers the creation of a file that contains the system state information, which can delay shutdown. Therefore, do not use zero for this parameter.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the required privilege (SE_SHUTDOWN_PRIVILEGE or SE_REMOTE_SHUTDOWN_PRIVILEGE) to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NETPATH</b></dt>
</dl>
</td>
<td width="60%">
The specified computer does not exist or is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_COMPUTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The specified  computer name is not a valid computer name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The specified computer does not support a shutdown interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid set of parameters was passed. This includes the following combinations.

<ul>
<li>The <i>lpMachineName</i> parameter specifies a remote computer, and the <i>dwShutdownFlags</i> parameter does not specify <b>SHUTDOWN_FORCE_SELF</b>.</li>
<li>The value of the <i>dwGracePeriod</i> is greater than zero and the <i>dwShutdownFlags</i> parameter does not specify <b>SHUTDOWN_FORCE_SELF</b>.</li>
<li>The value of the <i>dwGracePeriod</i> is greater than zero and the <i>dwShutdownFlags</i> parameter specifies <b>SHUTDOWN_GRACE_OVERRIDE</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A shutdown has already been started on the specified computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IS_SCHEDULED</b></dt>
</dl>
</td>
<td width="60%">
A shutdown for the specified computer has been scheduled but not started. For this function to succeed, the <b>SHUTDOWN_GRACE_OVERRIDE</b> flag must be set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_USERS_LOGGED_ON</b></dt>
</dl>
</td>
<td width="60%">
One or more users other than the current user are logged on the specified machine, and the <b>SHUTDOWN_FORCE_OTHERS</b> flag was not set.

</td>
</tr>
</table>

## -remarks

To shut down the local computer, the calling thread must have the SE_SHUTDOWN_NAME privilege. To shut down a remote computer, the calling thread must have the SE_REMOTE_SHUTDOWN_NAME privilege on the remote computer. By default, users can enable the SE_SHUTDOWN_NAME privilege on the computer they are logged onto, and administrators can enable the SE_REMOTE_SHUTDOWN_NAME privilege on remote computers. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Common reasons for failure include an invalid or inaccessible computer name or insufficient privilege. The error ERROR_SHUTDOWN_IN_PROGRESS is returned if a shutdown is already in progress on the specified computer. The error ERROR_NOT_READY can be returned if fast-user switching is enabled but no user is logged on.

A non-zero return value does not mean the logoff was or will be successful. The shutdown is an asynchronous process, and it can occur long  after the API call has returned, or not  at all. Even if the timeout value is zero,  the shutdown can still be aborted by applications, services, or even the system. The non-zero return value indicates that the validation of the rights and parameters was  successful and that the system accepted the shutdown request.





> [!NOTE]
> The winreg.h header defines InitiateShutdown as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>
