---
UID: NF:winbase.RegisterApplicationRestart
title: RegisterApplicationRestart function (winbase.h)
description: Registers the active instance of an application for restart.
helpviewer_keywords: ["RESTART_NO_CRASH","RESTART_NO_HANG","RESTART_NO_PATCH","RESTART_NO_REBOOT","RegisterApplicationRestart","RegisterApplicationRestart function [Recovery]","base.registerapplicationrestart","recovery.registerapplicationrestart","winbase/RegisterApplicationRestart"]
old-location: recovery\registerapplicationrestart.htm
tech.root: Recovery
ms.assetid: f4cd25b3-2aee-460f-9f9f-b45ecded094f
ms.date: 12/05/2018
ms.keywords: RESTART_NO_CRASH, RESTART_NO_HANG, RESTART_NO_PATCH, RESTART_NO_REBOOT, RegisterApplicationRestart, RegisterApplicationRestart function [Recovery], base.registerapplicationrestart, recovery.registerapplicationrestart, winbase/RegisterApplicationRestart
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterApplicationRestart
 - winbase/RegisterApplicationRestart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - Kernel32.dll
 - ext-ms-win-kernel32-windowserrorreporting-l1-1-1.dll
 - werapiexthost.dll
api_name:
 - RegisterApplicationRestart
---

# RegisterApplicationRestart function


## -description

Registers the active instance of an application for restart.

## -parameters

### -param pwzCommandline [in, optional]

A pointer to a Unicode string that specifies the command-line arguments for the application when it is restarted. The maximum size of the command line that you can specify is RESTART_MAX_CMD_LINE characters. Do not include the name of the executable in the command line; this function adds it for you.  

If this parameter is <b>NULL</b> or an empty string, the previously registered command line is removed. If the argument contains spaces, use quotes around the argument.

### -param dwFlags [in]

This parameter can be 0 or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESTART_NO_CRASH"></a><a id="restart_no_crash"></a><dl>
<dt><b>RESTART_NO_CRASH</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Do not restart the process if it terminates due to an unhandled exception.

</td>
</tr>
<tr>
<td width="40%"><a id="RESTART_NO_HANG"></a><a id="restart_no_hang"></a><dl>
<dt><b>RESTART_NO_HANG</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Do not restart the process if it terminates due to the  application not responding. 

</td>
</tr>
<tr>
<td width="40%"><a id="RESTART_NO_PATCH"></a><a id="restart_no_patch"></a><dl>
<dt><b>RESTART_NO_PATCH</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Do not restart the process if it terminates due to the installation of  an update.

</td>
</tr>
<tr>
<td width="40%"><a id="RESTART_NO_REBOOT"></a><a id="restart_no_reboot"></a><dl>
<dt><b>RESTART_NO_REBOOT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Do not restart the process if the computer is restarted as the result of an update.

</td>
</tr>
</table>

## -returns

This function returns <b>S_OK</b> on success or one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Internal error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified command line is too long.

</td>
</tr>
</table>

## -remarks

Your initial registration for restart must occur before the application encounters an unhandled exception or becomes unresponsive. You could then call this function from inside your recovery callback to update the command line.

For a Windows application that is being updated, the last opportunity to call this function is while processing the <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message. For a console application that is being updated, the registration must occur before the installer tries to shutdown the application (you need to keep the registration current; you cannot call this function when handling the CTRL_C_EVENT notification).

If you register for restart and the application encounters an unhandled exception or is not responsive, the user is offered the opportunity to restart the application; the application is not automatically restarted without the user's consent. However, if the application is being updated and requires a restart, the application is restarted automatically.

To prevent cyclical restarts, the system will only restart the application if it has been 
   	running for a minimum of 60 seconds.

Note that for an application to be restarted when the update requires a computer restart, the installer must call the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function with the EWX_RESTARTAPPS flag set or the <a href="/windows/desktop/api/winreg/nf-winreg-initiateshutdowna">InitiateShutdown</a> function with the SHUTDOWN_RESTARTAPPS flag set.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-unregisterapplicationrestart">UnregisterApplicationRestart</a>