---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NotifyServiceStatusChangeA function


## -description


Enables an application to receive notification when the specified service is created or deleted or when its status changes.


## -parameters




### -param hService [in]

A handle to the service or the service control manager. Handles to services are returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function and must have the SERVICE_QUERY_STATUS access right. Handles to the service control manager are returned by the <a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function and must have the SC_MANAGER_ENUMERATE_SERVICE access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.

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
Report when an application has specified the service in a call to the  <a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a> function. Your application should close any handles to the service so it can be deleted.

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

A pointer to a <a href="https://msdn.microsoft.com/52ede72e-eb50-48e2-b5c1-125816f6fe57">SERVICE_NOTIFY</a> structure that contains notification information, such as a pointer to the callback function. This structure must remain valid until the callback function is invoked or the calling thread cancels the notification request.

Do not make multiple calls to <b>NotifyServiceStatusChange</b> with the same buffer parameter until the callback function from the first call has finished with the buffer or the first notification request has been canceled. Otherwise, there is no guarantee which version of the buffer the callback function will receive.

<b>Windows Vista:  </b>The address of the callback function must be within the address range of a loaded module. Therefore, the callback function cannot be code that is generated at run time (such as managed code generated by the JIT compiler) or native code that is decompressed at run time. This restriction was removed in Windows Server 2008 and Windows Vista with SP1.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS. If the service has been marked for deletion, the return value is ERROR_SERVICE_MARKED_FOR_DELETE and the handle to the service must be closed. If service notification is lagging too far behind the system state, the function returns ERROR_SERVICE_NOTIFY_CLIENT_LAGGING. In this case, the client should close the handle to the SCM, open a new handle,  and call this function again. 

If the function fails, the return value is one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



 The <b>NotifyServiceStatusChange</b> function can be used to receive notifications about service applications. It cannot be used to receive notifications about driver services. 

When the service status changes, the system invokes the specified callback function as an asynchronous procedure call (APC) queued to the calling thread. The calling thread must enter an alertable wait (for example, by calling the <a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a> function) to receive notification. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540625">Asynchronous Procedure Calls</a>. 

If the service is already in any of the requested states when <b>NotifyServiceStatusChange</b> is called, the callback function is queued immediately. If the service state has not changed by the next time the function is called with the same service and state, the callback function is not queued immediately; the callback function is queued the next time the service enters the requested state.

The <b>NotifyServiceStatusChange</b> function calls the <a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a> function on the calling thread with the THREAD_SET_CONTEXT access right. If the calling thread does not have this access right, <b>NotifyServiceStatusChange</b> fails. If the calling thread is impersonating another user, it may not have sufficient permission to set context.

It is more efficient to call <b>NotifyServiceStatusChange</b> from a thread that performs a wait than to create an additional thread. 

After the callback function is invoked, the caller must call <b>NotifyServiceStatusChange</b> to receive additional notifications. Note that certain functions in the Windows API, including <b>NotifyServiceStatusChange</b> and other SCM functions,  use remote procedure calls (RPC); these functions might perform an alertable wait operation, so they are not safe to call from within the callback function. Instead, the callback function should save the notification parameters and perform any additional work outside the callback.

To cancel outstanding notifications, close the service handle using the <a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a> function. After <b>CloseServiceHandle</b> succeeds, no more notification APCs will be queued. If the calling  thread exits without closing the service handle or waiting until the APC  is generated, a memory leak can occur.

<div class="alert"><b>Important</b>  If the calling thread is in a DLL and the DLL is unloaded before the thread receives the notification or calls <a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a>, the notification will cause unpredictable results and might cause the process to stop responding.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/52ede72e-eb50-48e2-b5c1-125816f6fe57">SERVICE_NOTIFY</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

