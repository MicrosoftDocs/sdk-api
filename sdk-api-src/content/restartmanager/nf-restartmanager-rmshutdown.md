---
UID: NF:restartmanager.RmShutdown
title: RmShutdown function (restartmanager.h)
description: Initiates the shutdown of applications.
helpviewer_keywords: ["RmForceShutdown","RmShutdown","RmShutdown function [Restart Mgr]","RmShutdownOnlyRegistered","restartmanager/RmShutdown","rstmgr.rmshutdown"]
old-location: rstmgr\rmshutdown.htm
tech.root: rstmgr
ms.assetid: cdbc3bb7-0b3c-4fbc-8023-45a309c65bae
ms.date: 12/05/2018
ms.keywords: RmForceShutdown, RmShutdown, RmShutdown function [Restart Mgr], RmShutdownOnlyRegistered, restartmanager/RmShutdown, rstmgr.rmshutdown
req.header: restartmanager.h
req.include-header: 
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
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RmShutdown
 - restartmanager/RmShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-base-rstrtmgr-l1-1-0.dll
 - Rstrtmgr.dll
api_name:
 - RmShutdown
---

# RmShutdown function


## -description

Initiates the shutdown of applications.  This function can only be called from the installer that started the Restart Manager session using the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmstartsession">RmStartSession</a> function.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

### -param lActionFlags [in]

One or more   <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_shutdown_type">RM_SHUTDOWN_TYPE</a> options that configure the shut down of components. The following values can be combined by an OR operator to specify that unresponsive applications and services are to be forced to shut down if, and only if, all applications have been registered for restart.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RmForceShutdown"></a><a id="rmforceshutdown"></a><a id="RMFORCESHUTDOWN"></a><dl>
<dt><b>RmForceShutdown</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Force unresponsive applications and services to shut down after the timeout period. An application that does not respond to a shutdown request is forced to shut down within 30 seconds. A service that does not respond to a shutdown request is forced to shut down after 20 seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="RmShutdownOnlyRegistered"></a><a id="rmshutdownonlyregistered"></a><a id="RMSHUTDOWNONLYREGISTERED"></a><dl>
<dt><b>RmShutdownOnlyRegistered</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Shut down applications if and only if all the applications have been registered for restart  using the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function. If any processes or services cannot be restarted, then no processes or services are shut down.

</td>
</tr>
</table>

### -param fnStatus [in, optional]

A pointer to an <a href="/windows/desktop/api/restartmanager/nc-restartmanager-rm_write_status_callback">RM_WRITE_STATUS_CALLBACK</a> function that is used to communicate detailed status while this function is executing. If <b>NULL</b>, no status is provided.

## -returns

This is the most recent error received. The function can return one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> that are defined in Winerror.h. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All shutdown, restart, and callback operations were successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FAIL_NOACTION_REBOOT</b></dt>
<dt>350</dt>
</dl>
</td>
<td width="60%">
No shutdown actions were performed. One or more processes or services require a restart of the system to be shut down. This error code is returned when the Restart Manager detects that a restart of the system is required before shutting down any application.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FAIL_SHUTDOWN</b></dt>
<dt>351</dt>
</dl>
</td>
<td width="60%">
Some applications could not be shut down. The <b>AppStatus</b>  of the <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structures returned by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetlist">RmGetList</a> function contain updated status information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
<dt>1223</dt>
</dl>
</td>
<td width="60%">
 This error value is returned by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a> function when the request to cancel an operation is successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SEM_TIMEOUT</b></dt>
<dt>121</dt>
</dl>
</td>
<td width="60%">
A Restart Manager function could not obtain a Registry write mutex in the allotted time. A system restart is recommended because further use of the Restart Manager is likely to fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct.  This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
An operation was unable  to read or write to the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
A Restart Manager operation could not be completed because not enough memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
No Restart Manager session exists for the handle supplied.

</td>
</tr>
</table>

## -remarks

The <b>RmShutdown</b> function  calls <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetlist">RmGetList</a> and updates the list of processes currently using registered resources before attempting to shut down any processes. The  <b>RmShutdown</b> function then attempts to shut down the processes using registered resources in the most current list. The  <b>RmShutdown</b> function updates the <b>AppStatus</b>  member of the <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structures that are returned by the <b>RmGetList</b> function with detailed status information.

The Restart Manager respects the privileges that separate different user or terminal sessions. An installer that is running as a service with LocalSystem privileges cannot shut down or restart any applications in another user or terminal session.  Installers should implement custom methods to shut down and restart applications that are running in other sessions. One method would be to start a new   installer process  in the other session to perform shutdown and restart operations.

Installers should always restart application and services using the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a> function even when the <b>RmShutdown</b> function returns an error indicating that not all applications and services could be shut down.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmcancelcurrenttask">RmCancelCurrentTask</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a>