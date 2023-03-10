---
UID: NF:prnasnot.IPrintAsyncNotifyChannel.SendNotification
title: IPrintAsyncNotifyChannel::SendNotification (prnasnot.h)
description: Sends a notification from a component that is hosted by the print spooler to one or more listening applications, or sends a response from an application back to a component.
helpviewer_keywords: ["IPrintAsyncNotifyChannel interface [Windows GDI]","SendNotification method","IPrintAsyncNotifyChannel.SendNotification","IPrintAsyncNotifyChannel::SendNotification","SendNotification","SendNotification method [Windows GDI]","SendNotification method [Windows GDI]","IPrintAsyncNotifyChannel interface","_win32_IPrintAsyncNotifyChannel_SendNotification","gdi.iprintasyncnotifychannel_iprintasyncnotifychannel__sendnotification","prnasnot/IPrintAsyncNotifyChannel::SendNotification"]
old-location: gdi\iprintasyncnotifychannel_iprintasyncnotifychannel__sendnotification.htm
tech.root: xps
ms.assetid: 729286d4-75ee-441e-b63d-fef72d41533a
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyChannel interface [Windows GDI],SendNotification method, IPrintAsyncNotifyChannel.SendNotification, IPrintAsyncNotifyChannel::SendNotification, SendNotification, SendNotification method [Windows GDI], SendNotification method [Windows GDI],IPrintAsyncNotifyChannel interface, _win32_IPrintAsyncNotifyChannel_SendNotification, gdi.iprintasyncnotifychannel_iprintasyncnotifychannel__sendnotification, prnasnot/IPrintAsyncNotifyChannel::SendNotification
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
 - IPrintAsyncNotifyChannel::SendNotification
 - prnasnot/IPrintAsyncNotifyChannel::SendNotification
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
 - IPrintAsyncNotifyChannel.SendNotification
---

# IPrintAsyncNotifyChannel::SendNotification


## -description

Sends a notification from a component that is hosted by the print spooler to one or more listening applications, or sends a response from an application back to a component.

## -parameters

### -param pData [in]

A pointer to the content of the notification and its size and type.

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
<td>ASYNC_CALL_ALREADY_PARKED</td>
<td>ERROR</td>
<td>A notification cannot be sent because the recipient has not consumed the previous notification. </td>
</tr>
<tr>
<td>ASYNC_CALL_IN_PROGRESS</td>
<td>ERROR</td>
<td>The channel is busy with another notification or response.</td>
</tr>
<tr>
<td>ASYNC_NOTIFICATION_FAILURE</td>
<td>ERROR</td>
<td> None of the listeners on this channel are configured to receive this notification type or there was a problem allocating the resources necessary to complete this call.</td>
</tr>
<tr>
<td>CHANNEL_ACQUIRED</td>
<td>ERROR</td>
<td>Another listener has acquired this channel. The notification was not sent. The original listener will no longer receive notifications.</td>
</tr>
<tr>
<td>CHANNEL_ALREADY_CLOSED</td>
<td>ERROR</td>
<td>The notification could not be sent because the channel was closed prior to this call.</td>
</tr>
<tr>
<td>CHANNEL_NOT_OPENED</td>
<td>ERROR</td>
<td>The notification could not be sent because the channel was not opened prior to this call.</td>
</tr>
<tr>
<td>CHANNEL_WAITING_FOR_CLIENT_NOTIFICATION</td>
<td>ERROR</td>
<td>A notification cannot be sent because a response to the last notification has not been received.</td>
</tr>
<tr>
<td>INVALID_NOTIFICATION_TYPE</td>
<td>ERROR</td>
<td>The specified notification type is invalid.</td>
</tr>
<tr>
<td>MAX_NOTIFICATION_SIZE_EXCEEDED</td>
<td>ERROR</td>
<td>The maximum size of the notification data has been exceeded. By default, the maximum data size allowed is 10 megabytes. </td>
</tr>
<tr>
<td>NO_LISTENERS</td>
<td>SUCCESS</td>
<td>Indicates that there are no registered listening applications.</td>
</tr>
<tr>
<td>UNIRECTIONAL_NOTIFICATION_LOST</td>
<td>SUCCESS</td>
<td>One or more listeners did not receive this notification, but at least one listener did receive this notification. </td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an HRESULT other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific HRESULT that was returned by the function, use the HRESULT_CODE macro. The following code example shows how these macros can be used.

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.


```cpp
if (SUCCEEDED(hr)) {
  // Call succeeded, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case S_OK:
      // Some action 
      break;
    case NO_LISTENERS:
      // Some action 
      break;
    case UNIRECTIONAL_NOTIFICATION_LOST:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
} else {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case ASYNC_NOTIFICATION_FAILURE:
      // Some action 
      break;
    case CHANNEL_ALREADY_CLOSED:
      // Some action 
      break;
    case CHANNEL_NOT_OPENED:
      // Some action 
      break;
    //
    // ... Test for other error cases
    //    
    default:
      // Default action 
      break;
  }
}

```

## -remarks

For a unidirectional channel, if a <b>SendNotification</b> call is made while the print spooler is processing an earlier <b>SendNotification</b> call, the print spooler queues the pending notification. Queued notifications are discarded if either the component that is hosted by the print spooler or the application calls <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a>.

For a bidirectional channel, if a <b>SendNotification</b> call is made while the Print-Spooler is processing an earlier <b>SendNotification</b> call, then the pending call will fail. In that case, if the caller is a sender inside print spooler, <b>SendNotification</b> returns CHANNEL_WAITING_FOR_CLIENT_NOTIFICATION. If the caller is a listener sending a reply, then <b>SendNotification</b> returns ASYNC_CALL_IN_PROGRESS.

When multiple listeners exist for the same bidirectional channel, the initial notification sent on the channel will be delivered to all listeners. The first listener to reply will acquire the channel. Listeners calling <b>SendNotification</b> after the channel was acquired will fail with error CHANNEL_ACQUIRED.

A listener receiving an initial notification on a bidirectional channel might not be interested in acquiring the channel. In this case the listener can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method can be called. The <b>IUnknown::Release</b> method does not need to be called if <b>SendNotification</b> or <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a> methods are called.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel">IPrintAsyncNotifyChannel</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>