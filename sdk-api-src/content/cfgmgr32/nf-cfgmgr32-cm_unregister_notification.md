---
UID: NF:cfgmgr32.CM_Unregister_Notification
title: CM_Unregister_Notification function
author: windows-sdk-content
description: Use UnregisterDeviceNotification instead of CM_Unregister_Notification if your code targets Windows 7 or earlier versions of Windows.
old-location: devinst\cm_unregister_notification.htm
old-project: devinst
ms.assetid: 1634ECC5-96A2-4B1C-8DCA-64682C8C1444
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CM_Unregister_Notification, CM_Unregister_Notification function [Device and Driver Installation], cfgmgr32/CM_Unregister_Notification, devinst.cm_unregister_notification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 8 and later versions of Windows.
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Unregister_Notification
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Unregister_Notification function


## -description


Use <a href="https://msdn.microsoft.com/en-us/library/Aa363475(v=VS.85).aspx">UnregisterDeviceNotification</a> instead of <b>CM_Unregister_Notification</b> if your code targets Windows 7 or earlier versions of Windows.

The <b>CM_Unregister_Notification</b> function closes the specified HCMNOTIFICATION handle.


## -parameters




### -param NotifyContext [in]

The HCMNOTIFICATION handle returned by the <a href="https://msdn.microsoft.com/en-us/library/Hh780224(v=VS.85).aspx">CM_Register_Notification</a> function.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Do not call <b>CM_Unregister_Notification</b> from a notification callback. Doing so may cause a deadlock because <b>CM_Unregister_Notification</b> waits for pending callbacks to finish.

Instead, if you want to unregister from the notification callback, you must do so asynchronously.       The following sequence shows one way to do this:

<ol>
<li>Allocate a context structure to use with your notifications.      Include a pointer to a threadpool work structure (<b>PTP_WORK</b>) and any other information you would like to pass to the notification callback.</li>
<li>Call <a href="https://msdn.microsoft.com/library/windows/desktop/ms682478">CreateThreadpoolWork</a>.   Provide a callback function that calls  <b>CM_Unregister_Notification</b>.      Add the returned work structure to the previously allocated context structure.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Hh780224(v=VS.85).aspx">CM_Register_Notification</a> and provide the context structure as the <i>pContext</i> parameter.</li>
<li>Do work, get notifications, etc.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/ms686338(v=VS.85).aspx">SubmitThreadpoolWork</a> from within the notification callback, providing the pointer to a threadpool work structure (<b>PTP_WORK</b>) stored in your context structure.</li>
<li>When the threadpool thread runs, the work item calls <b>CM_Unregister_Notification</b>.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/ms682043(v=VS.85).aspx">CloseThreadpoolWork</a> to release the work object.</li>
</ol>
If you are finished with the context structure, don't forget to release resources and and free the structure.

<div class="alert"><b>Caution</b>  Do not free the context structure until after the work item has called <b>CM_Unregister_Notification</b>.  You can still receive notifications after submitting the threadpool work item and before the work item calls <b>CM_Unregister_Notification</b>.</div>
<div> </div>

#### Examples

The following example shows how to unregister from the notification callback, as described in the Remarks section.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _CALLBACK_CONTEXT {
    BOOL bUnregister;
    PTP_WORK pWork;
    HCMNOTIFICATION hNotify;
    CRITICAL_SECTION lock;
} CALLBACK_CONTEXT, *PCALLBACK_CONTEXT;

DWORD
WINAPI
EventCallback(
    __in HCMNOTIFICATION hNotification,
    __in PVOID Context,
    __in CM_NOTIFY_ACTION Action,
    __in PCM_NOTIFY_EVENT_DATA EventData,
    __in DWORD EventDataSize
    )
{
    PCALLBACK_CONTEXT pCallbackContext = (PCALLBACK_CONTEXT)Context;

   // unregister from the callback
    EnterCriticalSection(&amp;(pCallbackContext-&gt;lock));

    // in case this callback fires before the registration call returns, make sure the notification handle is properly set
    Context-&gt;hNotify = hNotification;

    if (!pCallbackContext-&gt;bUnregister) {
        pCallbackContext-&gt;bUnregister = TRUE;
        SubmitThreadpoolWork(pCallbackContext-&gt;pWork);
    }

    LeaveCriticalSection(&amp;(pCallbackContext-&gt;lock));

    return ERROR_SUCCESS;
};

VOID
CALLBACK
WorkCallback(
    _Inout_ PTP_CALLBACK_INSTANCE Instance,
    _Inout_opt_ PVOID Context,
    _Inout_ PTP_WORK pWork
    )
{
    PCALLBACK_CONTEXT pCallbackContext = (PCALLBACK_CONTEXT)Context;

    CM_Unregister_Notification(pCallbackContext-&gt;hNotify);
}

VOID NotificationFunction()
{
    CONFIGRET cr = CR_SUCCESS;
    HRESULT hr = S_OK;
    CM_NOTIFY_FILTER NotifyFilter = { 0 };
    BOOL bShouldUnregister = FALSE;
    PCALLBACK_CONTEXT context;

    context = (PCALLBACK_CONTEXT)HeapAlloc(GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof(CALLBACK_CONTEXT));
    if (context == NULL) {
        goto end;
    }

    InitializeCriticalSection(&amp;(context-&gt;lock));

    NotifyFilter.cbSize = sizeof(NotifyFilter);
    NotifyFilter.Flags = 0;
    NotifyFilter.FilterType = CM_NOTIFY_FILTER_TYPE_DEVICEINSTANCE;
    NotifyFilter.Reserved = 0;

    hr = StringCchCopy(NotifyFilter.u.DeviceInstance.InstanceId,
                       MAX_DEVICE_ID_LEN,
                       TEST_DEVICE_INSTANCE_ID);
    if (FAILED(hr)) {
        goto end;
    }

    context-&gt;pWork = CreateThreadpoolWork(WorkCallback, context, NULL);
    if (context-&gt;pWork == NULL) {
        goto end;
    }

    cr = CM_Register_Notification(&amp;NotifyFilter,
                                  context,
                                  EventCallback,
                                  &amp;context-&gt;hNotify);
   if (cr != CR_SUCCESS) {
        goto end;
    }

    // ... do work here ...

    EnterCriticalSection(&amp;(context-&gt;lock));

    if (!context-&gt;bUnregister) {
        // unregister not from the callback
        bShouldUnregister = TRUE;
        context-&gt;bUnregister = TRUE;
    }

    LeaveCriticalSection(&amp;(context-&gt;lock));

    if (bShouldUnregister) {
        cr = CM_Unregister_Notification(context-&gt;hNotify);
        if (cr != CR_SUCCESS) {
            goto end;
        }
    } else {
        // if the callback is the one performing the unregister, wait for the threadpool work item to complete the unregister
        WaitForThreadpoolWorkCallbacks(context-&gt;pWork, FALSE);
    }

end:

    if (context != NULL) {
        if (context-&gt;pWork != NULL) {
            CloseThreadpoolWork(context-&gt;pWork);
        }

        DeleteCriticalSection(&amp;(context-&gt;lock));

        HeapFree(GetProcessHeap(), 0, context);
    }

    return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363475(v=VS.85).aspx">UnregisterDeviceNotification</a>
 

 

