---
UID: NF:wtsapi32.WTSShutdownSystem
title: WTSShutdownSystem function (wtsapi32.h)
description: Shuts down (and optionally restarts) the specified Remote Desktop Session Host (RD Session Host) server.
helpviewer_keywords: ["WTSShutdownSystem","WTSShutdownSystem function [Remote Desktop Services]","WTS_WSD_FASTREBOOT","WTS_WSD_LOGOFF","WTS_WSD_POWEROFF","WTS_WSD_REBOOT","WTS_WSD_SHUTDOWN","_win32_wtsshutdownsystem","termserv.wtsshutdownsystem","wtsapi32/WTSShutdownSystem"]
old-location: termserv\wtsshutdownsystem.htm
tech.root: TermServ
ms.assetid: 188df0d6-0e49-4608-bc70-83775584a1f2
ms.date: 12/05/2018
ms.keywords: WTSShutdownSystem, WTSShutdownSystem function [Remote Desktop Services], WTS_WSD_FASTREBOOT, WTS_WSD_LOGOFF, WTS_WSD_POWEROFF, WTS_WSD_REBOOT, WTS_WSD_SHUTDOWN, _win32_wtsshutdownsystem, termserv.wtsshutdownsystem, wtsapi32/WTSShutdownSystem
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSShutdownSystem
 - wtsapi32/WTSShutdownSystem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSShutdownSystem
---

# WTSShutdownSystem function


## -description

Shuts down (and optionally restarts) the specified Remote Desktop Session Host (RD Session Host) server.

To shut down or restart the system, the calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege enabled. For more information about security privileges, see 
<a href="/windows/desktop/SecAuthZ/privileges">Privileges</a> and 
<a href="/windows/desktop/SecAuthZ/authorization-constants">Authorization Constants</a>.

## -parameters

### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is running.

### -param ShutdownFlag [in]

Indicates the type of shutdown. This parameter can be one of the following values.



#### WTS_WSD_LOGOFF

Forces all client sessions to log off (except the session calling 
<b>WTSShutdownSystem</b>) and disables any subsequent remote logons. This can be used as a step before shutting down. Logons will be re-enabled when the Remote Desktop Services service is restarted.

Use this value only on the Remote Desktop Services console.



#### WTS_WSD_POWEROFF

Shuts down the system on the RD Session Host server and, on computers that support software control of AC power, turns off the power. This is equivalent to calling <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> with <b>EWX_SHUTDOWN</b> and <b>EWX_POWEROFF</b>. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege enabled.



#### WTS_WSD_REBOOT

Shuts down and then restarts the system on the RD Session Host server. This is equivalent to calling <b>ExitWindowsEx</b> with <b>EWX_REBOOT</b>. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege enabled.



#### WTS_WSD_SHUTDOWN

Shuts down the system on the RD Session Host server. This is equivalent to calling the 
<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function with <b>EWX_SHUTDOWN</b>. The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege enabled.



#### WTS_WSD_FASTREBOOT

This value is not supported currently.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A system shutdown terminates all users and active programs. The following steps occur during shutdown.

<ol>
<li>An exit command is issued to all active user applications.</li>
<li>If the application does not exit within a specific interval, the application is terminated.</li>
<li>After all the applications for a user terminate, the user is logged off.</li>
<li>After all users are logged off, an exit command is issued to all system services.</li>
<li>If the system service does not terminate within a specific interval, the service is terminated.</li>
<li>The file system cache is written to disk.</li>
<li>The disks are marked read-only.</li>
<li>The RD Session Host server displays the message "It is now safe to turn off your computer", or the system is restarted if <b>WTS_WSD_REBOOT</b> is specified. (The message is displayed on the console because all client sessions have been terminated.)</li>
</ol>
<div class="alert"><b>Note</b>  Because there can be many users and processes in a large multiple-user configuration, large system configurations may take some time to shut down in an orderly fashion. It is important to allow the system to shut down completely.</div>
<div> </div>
<b>Windows Server 2008 and Windows Vista:  </b>A call to <b>WTSShutdownSystem</b> does not work when Remote Connection Manager (RCM) is disabled. This is the case when the Remote Desktop Services service is stopped.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>