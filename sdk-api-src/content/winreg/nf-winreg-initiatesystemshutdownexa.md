---
UID: NF:winreg.InitiateSystemShutdownExA
title: InitiateSystemShutdownExA function (winreg.h)
description: Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown. (ANSI)
helpviewer_keywords: ["InitiateSystemShutdownExA", "winreg/InitiateSystemShutdownExA"]
old-location: base\initiatesystemshutdownex.htm
tech.root: base
ms.assetid: 4536cf76-7669-42b1-8c44-9f5e368424cc
ms.date: 12/05/2018
ms.keywords: InitiateSystemShutdownEx, InitiateSystemShutdownEx function, InitiateSystemShutdownExA, InitiateSystemShutdownExW, _win32_initiatesystemshutdownex, base.initiatesystemshutdownex, winreg/InitiateSystemShutdownEx, winreg/InitiateSystemShutdownExA, winreg/InitiateSystemShutdownExW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InitiateSystemShutdownExW (Unicode) and InitiateSystemShutdownExA (ANSI)
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
 - InitiateSystemShutdownExA
 - winreg/InitiateSystemShutdownExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-shutdown-ansi-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-shutdown-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-shutdown-l1-1-1.dll
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - Ext-MS-Win-AdvAPI32-shutdown-l1-1-0.dll
api_name:
 - InitiateSystemShutdownEx
 - InitiateSystemShutdownExA
 - InitiateSystemShutdownExW
---

# InitiateSystemShutdownExA function


## -description

Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.

## -parameters

### -param lpMachineName [in, optional]

The network name of the computer to be shut down. If <i>lpMachineName</i> is <b>NULL</b> or an empty string, the function shuts down the local computer.

### -param lpMessage [in, optional]

The message to be displayed in the shutdown dialog box. This parameter can be <b>NULL</b> if no message is required. 




<b>Windows Server 2003 and Windows XP:  </b>This string is also stored as a comment in the event log entry.

<b>Windows Server 2003 and Windows XP with SP1:  </b>The string is limited to 3072 <b>TCHARs</b>.

### -param dwTimeout [in]

The length of time that the shutdown dialog box should be displayed, in seconds. While this dialog box is displayed, shutdown can be stopped by the 
<a href="/windows/desktop/api/winreg/nf-winreg-abortsystemshutdowna">AbortSystemShutdown</a> function. 




If <i>dwTimeout</i> is not zero, 
<b>InitiateSystemShutdownEx</b> displays a dialog box on the specified computer. The dialog box displays the name of the user who called the function, displays the message specified by the <i>lpMessage</i> parameter, and prompts the user to log off. The dialog box beeps when it is created and remains on top of other windows in the system. The dialog box can be moved but not closed. A timer counts down the remaining time before shutdown.

If <i>dwTimeout</i> is zero, the computer shuts down without displaying the dialog box, and the shutdown cannot be stopped by 
<a href="/windows/desktop/api/winreg/nf-winreg-abortsystemshutdowna">AbortSystemShutdown</a>.

<b>Windows Server 2003 and Windows XP with SP1:  </b>The time-out value is limited to MAX_SHUTDOWN_TIMEOUT seconds.

<b>Windows Server 2003 and Windows XP with SP1:  </b>If the computer to be shut down is a Terminal Services server, the system displays a dialog box to all local and remote users warning them that shutdown has been initiated. The dialog box includes who requested the shutdown, the display message (see <i>lpMessage</i>), and how much time there is until the server is shut down.

### -param bForceAppsClosed [in]

If this parameter is <b>TRUE</b>, applications with unsaved changes are to be forcibly closed. If this parameter is <b>FALSE</b>, the system displays a dialog box instructing the user to close the applications.

### -param bRebootAfterShutdown [in]

If this parameter is <b>TRUE</b>, the computer is to restart immediately after shutting down. If this parameter is <b>FALSE</b>, the system flushes all caches to disk  and  safely powers down the system.

### -param dwReason [in]

The reason for initiating the shutdown. This parameter must be one of the 
<a href="/windows/desktop/Shutdown/system-shutdown-reason-codes">system shutdown reason codes</a>. 




If this parameter is zero, the default is an undefined shutdown that is logged as "No title for this reason could be found". By default, it is also an unplanned shutdown. Depending on how the system is configured, an unplanned shutdown triggers the creation of a file that contains the system state information, which can delay shutdown. Therefore, do not use zero for this parameter.

<b>Windows XP:  </b>System state information is not saved during an unplanned system shutdown. The preceding text does not apply.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To shut down the local computer, the calling thread must have the SE_SHUTDOWN_NAME privilege. To shut down a remote computer, the calling thread must have the SE_REMOTE_SHUTDOWN_NAME privilege on the remote computer. By default, users can enable the SE_SHUTDOWN_NAME privilege on the computer they are logged onto, and administrators can enable the SE_REMOTE_SHUTDOWN_NAME privilege on remote computers. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Common reasons for failure include an invalid or inaccessible computer name or insufficient privilege. The error ERROR_SHUTDOWN_IN_PROGRESS is returned if a shutdown is already in progress on the specified computer. The error ERROR_NOT_READY can be returned if fast-user switching is enabled but no user is logged on.

A non-zero return value does not mean the logoff was or will be successful. The shutdown is an asynchronous process, and it can occur long  after the API call has returned, or not  at all. Even if the timeout value is zero,  the shutdown can still be aborted by applications, services, or even the system. The non-zero return value indicates that the validation of the rights and parameters was  successful and that the system accepted the shutdown request.

When this function is called, the caller must specify whether or not applications with unsaved changes should be forcibly closed.  If the caller chooses not to force these applications to close and an application with unsaved changes is running on the console session, the shutdown will remain in progress until the user logged into the console session aborts the shutdown, saves changes, closes the application, or forces the application to close.  During this period the shutdown may not be aborted except by the console user, and another shutdown may not be initiated.

Note that calling this function with the value of the <i>bForceAppsClosed</i> parameter set to <b>TRUE</b> avoids this situation. Remember that doing this  may result in loss of data.

<b>Windows Server 2003 and Windows XP:  </b>If the computer is locked and the <i>bForceAppsClosed</i> parameter is <b>FALSE</b>, the last error code is ERROR_MACHINE_LOCKED. If the system is not ready to handle the request, the last error code is ERROR_NOT_READY. The application should wait a short while and retry the call. For example, the system can be unready to initiate a shutdown, and return ERROR_NOT_READY,  if the shutdown request comes at the same time a user tries to log onto the system. In this case, the application should wait a short while and retry the call.





> [!NOTE]
> The winreg.h header defines InitiateSystemShutdownEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-abortsystemshutdowna">AbortSystemShutdown</a>



<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>



<a href="/windows/desktop/Shutdown/system-shutdown-functions">System Shutdown Functions</a>
