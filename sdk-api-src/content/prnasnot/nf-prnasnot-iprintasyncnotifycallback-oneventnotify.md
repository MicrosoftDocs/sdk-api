---
UID: NF:prnasnot.IPrintAsyncNotifyCallback.OnEventNotify
title: IPrintAsyncNotifyCallback::OnEventNotify (prnasnot.h)
description: Alerts a listener that a notification is available on a specified channel. This method is called by the print system.
helpviewer_keywords: ["IPrintAsyncNotifyCallback interface [Windows GDI]","OnEventNotify method","IPrintAsyncNotifyCallback.OnEventNotify","IPrintAsyncNotifyCallback::OnEventNotify","OnEventNotify","OnEventNotify method [Windows GDI]","OnEventNotify method [Windows GDI]","IPrintAsyncNotifyCallback interface","_win32_IPrintAsyncNotifyCallback_OnEventNotify","gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__oneventnotify","prnasnot/IPrintAsyncNotifyCallback::OnEventNotify"]
old-location: gdi\iprintasyncnotifycallback_iprintasyncnotifycallback__oneventnotify.htm
tech.root: xps
ms.assetid: 2f398173-3cd6-46da-931d-057d1dccbe9b
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyCallback interface [Windows GDI],OnEventNotify method, IPrintAsyncNotifyCallback.OnEventNotify, IPrintAsyncNotifyCallback::OnEventNotify, OnEventNotify, OnEventNotify method [Windows GDI], OnEventNotify method [Windows GDI],IPrintAsyncNotifyCallback interface, _win32_IPrintAsyncNotifyCallback_OnEventNotify, gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__oneventnotify, prnasnot/IPrintAsyncNotifyCallback::OnEventNotify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintAsyncNotifyCallback::OnEventNotify
 - prnasnot/IPrintAsyncNotifyCallback::OnEventNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyCallback.OnEventNotify
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

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

The following code example shows how these macros can be used to evaluate the return value.


```cpp
if (SUCCEEDED(hr)){
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

```

## -remarks

To deliver a notification, the print spooler will call the <b>OnEventNotify</b> method of the <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback">IPrintAsyncNotifyCallback</a> object provided by the listening application at the time it registered for notifications. For unidirectional notifications, <i>pChannel</i> is <b>NULL</b>. For bidirectional channels, <i>pChannel</i> points to an <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel">IPrintAsyncNotifyChannel</a> to be used by a listening application to send a notification in response. The listener will do this by calling the <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">SendNotification</a> method of the <b>IPrintAsyncNotifyChannel</b>.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>



<a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback">IPrintAsyncNotifyCallback</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>