---
UID: NF:winsvc.NotifyServiceStatusChangeA
title: NotifyServiceStatusChangeA function (winsvc.h)
description: Enables an application to receive notification when the specified service is created or deleted or when its status changes. (ANSI)
helpviewer_keywords: ["NotifyServiceStatusChangeA", "SERVICE_NOTIFY_CONTINUE_PENDING", "SERVICE_NOTIFY_CREATED", "SERVICE_NOTIFY_DELETED", "SERVICE_NOTIFY_DELETE_PENDING", "SERVICE_NOTIFY_PAUSED", "SERVICE_NOTIFY_PAUSE_PENDING", "SERVICE_NOTIFY_RUNNING", "SERVICE_NOTIFY_START_PENDING", "SERVICE_NOTIFY_STOPPED", "SERVICE_NOTIFY_STOP_PENDING", "winsvc/NotifyServiceStatusChangeA"]
old-location: base\notifyservicestatuschange.htm
tech.root: security
ms.assetid: e22b7f69-f096-486f-97fa-0465bef499cd
ms.date: 12/05/2018
ms.keywords: NotifyServiceStatusChange, NotifyServiceStatusChange function, NotifyServiceStatusChangeA, NotifyServiceStatusChangeW, SERVICE_NOTIFY_CONTINUE_PENDING, SERVICE_NOTIFY_CREATED, SERVICE_NOTIFY_DELETED, SERVICE_NOTIFY_DELETE_PENDING, SERVICE_NOTIFY_PAUSED, SERVICE_NOTIFY_PAUSE_PENDING, SERVICE_NOTIFY_RUNNING, SERVICE_NOTIFY_START_PENDING, SERVICE_NOTIFY_STOPPED, SERVICE_NOTIFY_STOP_PENDING, base.notifyservicestatuschange, winsvc/NotifyServiceStatusChange, winsvc/NotifyServiceStatusChangeA, winsvc/NotifyServiceStatusChangeW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NotifyServiceStatusChangeW (Unicode) and NotifyServiceStatusChangeA (ANSI)
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
 - NotifyServiceStatusChangeA
 - winsvc/NotifyServiceStatusChangeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-management-l2-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - NotifyServiceStatusChange
 - NotifyServiceStatusChangeA
 - NotifyServiceStatusChangeW
---

# NotifyServiceStatusChangeA function


## -description

Enables an application to receive notification when the specified service is created or deleted or when its status changes.

## -parameters

### -param hService [in]

A handle to the service or the service control manager. Handles to services are returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openservicea">OpenService</a> or <a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function and must have the SERVICE_QUERY_STATUS access right. Handles to the service control manager are returned by the <a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function and must have the SC_MANAGER_ENUMERATE_SERVICE access right. For more information, see 
<a href="/windows/desktop/Services/service-security-and-access-rights">Service Security and Access Rights</a>.

There can only be one outstanding notification request per service.

### -param dwNotifyMask [in]

The type of status changes that should be reported. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_CREATED"></a><a id="service_notify_created"></a><dl>
<dt><b>SERVICE_NOTIFY_CREATED</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Report when the service has been created. 

The <i>hService</i> parameter must be a handle to the SCM.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_CONTINUE_PENDING"></a><a id="service_notify_continue_pending"></a><dl>
<dt><b>SERVICE_NOTIFY_CONTINUE_PENDING</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Report when the service is about to continue.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_DELETE_PENDING"></a><a id="service_notify_delete_pending"></a><dl>
<dt><b>SERVICE_NOTIFY_DELETE_PENDING</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Report when an application has specified the service in a call to the  <a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a> function. Your application should close any handles to the service so it can be deleted.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_DELETED"></a><a id="service_notify_deleted"></a><dl>
<dt><b>SERVICE_NOTIFY_DELETED</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Report when the service has been deleted. An application cannot receive this notification if it has an open handle to the service.

The <i>hService</i> parameter must be a handle to the SCM.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_PAUSE_PENDING"></a><a id="service_notify_pause_pending"></a><dl>
<dt><b>SERVICE_NOTIFY_PAUSE_PENDING</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Report when the service is pausing.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_PAUSED"></a><a id="service_notify_paused"></a><dl>
<dt><b>SERVICE_NOTIFY_PAUSED</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Report when the service has paused.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_RUNNING"></a><a id="service_notify_running"></a><dl>
<dt><b>SERVICE_NOTIFY_RUNNING</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Report when the service is running.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_START_PENDING"></a><a id="service_notify_start_pending"></a><dl>
<dt><b>SERVICE_NOTIFY_START_PENDING</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Report when the service is starting.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_STOP_PENDING"></a><a id="service_notify_stop_pending"></a><dl>
<dt><b>SERVICE_NOTIFY_STOP_PENDING</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Report when the service is stopping.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NOTIFY_STOPPED"></a><a id="service_notify_stopped"></a><dl>
<dt><b>SERVICE_NOTIFY_STOPPED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Report when the service has stopped.

The <i>hService</i> parameter must be a handle to the service.

</td>
</tr>
</table>

### -param pNotifyBuffer [in]

A pointer to a <a href="/windows/desktop/api/winsvc/ns-winsvc-service_notify_2a">SERVICE_NOTIFY</a> structure that contains notification information, such as a pointer to the callback function. This structure must remain valid until the callback function is invoked or the calling thread cancels the notification request.

Do not make multiple calls to <b>NotifyServiceStatusChange</b> with the same buffer parameter until the callback function from the first call has finished with the buffer or the first notification request has been canceled. Otherwise, there is no guarantee which version of the buffer the callback function will receive.

<b>Windows Vista:  </b>The address of the callback function must be within the address range of a loaded module. Therefore, the callback function cannot be code that is generated at run time (such as managed code generated by the JIT compiler) or native code that is decompressed at run time. This restriction was removed in Windows Server 2008 and Windows Vista with SP1.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS. If the service has been marked for deletion, the return value is ERROR_SERVICE_MARKED_FOR_DELETE and the handle to the service must be closed. If service notification is lagging too far behind the system state, the function returns ERROR_SERVICE_NOTIFY_CLIENT_LAGGING. In this case, the client should close the handle to the SCM, open a new handle,  and call this function again. 

If the function fails, the return value is one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

 The <b>NotifyServiceStatusChange</b> function can be used to receive notifications about service applications. It cannot be used to receive notifications about driver services. 

When the service status changes, the system invokes the specified callback function as an asynchronous procedure call (APC) queued to the calling thread. The calling thread must enter an alertable wait (for example, by calling the <a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a> function) to receive notification. For more information, see <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>. 

If the service is already in any of the requested states when <b>NotifyServiceStatusChange</b> is called, the callback function is queued immediately. If the service state has not changed by the next time the function is called with the same service and state, the callback function is not queued immediately; the callback function is queued the next time the service enters the requested state.

The <b>NotifyServiceStatusChange</b> function calls the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a> function on the calling thread with the THREAD_SET_CONTEXT access right. If the calling thread does not have this access right, <b>NotifyServiceStatusChange</b> fails. If the calling thread is impersonating another user, it may not have sufficient permission to set context.

It is more efficient to call <b>NotifyServiceStatusChange</b> from a thread that performs a wait than to create an additional thread. 

After the callback function is invoked, the caller must call <b>NotifyServiceStatusChange</b> to receive additional notifications. Note that certain functions in the Windows API, including <b>NotifyServiceStatusChange</b> and other SCM functions,  use remote procedure calls (RPC); these functions might perform an alertable wait operation, so they are not safe to call from within the callback function. Instead, the callback function should save the notification parameters and perform any additional work outside the callback.

To cancel outstanding notifications, close the service handle using the <a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a> function. After <b>CloseServiceHandle</b> succeeds, no more notification APCs will be queued. If the calling  thread exits without closing the service handle or waiting until the APC  is generated, a memory leak can occur.

<div class="alert"><b>Important</b>  If the calling thread is in a DLL and the DLL is unloaded before the thread receives the notification or calls <a href="/windows/desktop/api/winsvc/nf-winsvc-closeservicehandle">CloseServiceHandle</a>, the notification will cause unpredictable results and might cause the process to stop responding.</div>
<div> </div>




> [!NOTE]
> The winsvc.h header defines NotifyServiceStatusChange as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/ns-winsvc-service_notify_2a">SERVICE_NOTIFY</a>

<a href="/windows/desktop/services/subscribeservicechangenotifications">SubscribeServiceChangeNotifications</a>

<a href="/windows/desktop/Services/service-functions">Service Functions</a>
