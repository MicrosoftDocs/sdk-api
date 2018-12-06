---
UID: NF:prnasnot.IPrintAsyncNotifyCallback.OnEventNotify
title: IPrintAsyncNotifyCallback::OnEventNotify
author: windows-sdk-content
description: Alerts a listener that a notification is available on a specified channel. This method is called by the print system.
old-location: gdi\iprintasyncnotifycallback_iprintasyncnotifycallback__oneventnotify.htm
tech.root: printdocs
ms.assetid: 2f398173-3cd6-46da-931d-057d1dccbe9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPrintAsyncNotifyCallback interface [Windows GDI],OnEventNotify method, IPrintAsyncNotifyCallback.OnEventNotify, IPrintAsyncNotifyCallback::OnEventNotify, OnEventNotify, OnEventNotify method [Windows GDI], OnEventNotify method [Windows GDI],IPrintAsyncNotifyCallback interface, _win32_IPrintAsyncNotifyCallback_OnEventNotify, gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__oneventnotify, prnasnot/IPrintAsyncNotifyCallback::OnEventNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: prnasnot.h
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
req.lib: 
req.dll: Prnasnot.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyCallback.OnEventNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintAsyncNotifyCallback::OnEventNotify


## -description


Alerts a listener that a notification is available on a specified channel. This method is called by the print system.


## -parameters




### -param pChannel [in]

A pointer to the channel used by the sender and the listener.


### -param pData [in]

A pointer to the object that contains the notification data and its size and type.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Severity</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>SUCCESS</td>
<td>The function completed successfully.</td>
</tr>
<tr>
<td>INTERNAL_NOTIFICATION_QUEUE_IS_FULL</td>
<td>ERROR</td>
<td>The Print Spooler cannot hold any more queued notifications. By default, the maximum size of the queue is 10 notifications. When this error is returned, the listening application is not processing the notifications as fast as they are being sent. This notification should either be resent or discarded. </td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an HRESULT other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific HRESULT that was returned by the function, use the HRESULT_CODE macro.

See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="_com_error_handling">Error Handling</a>.

The following code example shows how these macros can be used to evaluate the return value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr)){
  // Call was successful 
}

if (FAILED(hr)) {
  // Call failed 
}

if (FAILED(hr)) {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case INTERNAL_NOTIFICATION_QUEUE_IS_FULL:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
} else {
  // Call succeeded 
}
</pre>
</td>
</tr>
</table></span></div>



## -remarks



To deliver a notification, the print spooler will call the <b>OnEventNotify</b> method of the <a href="https://msdn.microsoft.com/e2b021cd-1cfd-42b7-b6e4-7f8671b013f6">IPrintAsyncNotifyCallback</a> object provided by the listening application at the time it registered for notifications. For unidirectional notifications, <i>pChannel</i> is <b>NULL</b>. For bidirectional channels, <i>pChannel</i> points to an <a href="https://msdn.microsoft.com/8973cf5a-bbce-43c2-b418-2807842d43c0">IPrintAsyncNotifyChannel</a> to be used by a listening application to send a notification in response. The listener will do this by calling the <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">SendNotification</a> method of the <b>IPrintAsyncNotifyChannel</b>.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="_com_error_handling">Error Handling</a>



<a href="https://msdn.microsoft.com/e2b021cd-1cfd-42b7-b6e4-7f8671b013f6">IPrintAsyncNotifyCallback</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

