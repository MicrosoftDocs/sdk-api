---
UID: NF:prnasnot.IPrintAsyncNotifyChannel.CloseChannel
title: IPrintAsyncNotifyChannel::CloseChannel (prnasnot.h)
description: Closes the channel. (IPrintAsyncNotifyChannel.CloseChannel)
helpviewer_keywords: ["CloseChannel","CloseChannel method [Windows GDI]","CloseChannel method [Windows GDI]","IPrintAsyncNotifyChannel interface","IPrintAsyncNotifyChannel interface [Windows GDI]","CloseChannel method","IPrintAsyncNotifyChannel.CloseChannel","IPrintAsyncNotifyChannel::CloseChannel","_win32_IPrintAsyncNotifyChannel_CloseChannel","gdi.iprintasyncnotifychannel_iprintasyncnotifychannel__closechannel","prnasnot/IPrintAsyncNotifyChannel::CloseChannel"]
old-location: gdi\iprintasyncnotifychannel_iprintasyncnotifychannel__closechannel.htm
tech.root: xps
ms.assetid: d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7
ms.date: 12/05/2018
ms.keywords: CloseChannel, CloseChannel method [Windows GDI], CloseChannel method [Windows GDI],IPrintAsyncNotifyChannel interface, IPrintAsyncNotifyChannel interface [Windows GDI],CloseChannel method, IPrintAsyncNotifyChannel.CloseChannel, IPrintAsyncNotifyChannel::CloseChannel, _win32_IPrintAsyncNotifyChannel_CloseChannel, gdi.iprintasyncnotifychannel_iprintasyncnotifychannel__closechannel, prnasnot/IPrintAsyncNotifyChannel::CloseChannel
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
 - IPrintAsyncNotifyChannel::CloseChannel
 - prnasnot/IPrintAsyncNotifyChannel::CloseChannel
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
 - IPrintAsyncNotifyChannel.CloseChannel
---

# IPrintAsyncNotifyChannel::CloseChannel


## -description

Closes the channel.

## -parameters

### -param pData [in]

Pointer to a notification that specifies why the channel closed. This pointer can be <b>NULL</b>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Severity</th>
<th>Meaning</th>
</tr>
<tr>
<td>
S_OK

</td>
<td>
SUCCESS

</td>
<td>
The function completed successfully.

</td>
</tr>
<tr>
<td>
CHANNEL_ACQUIRED

</td>
<td>
ERROR

or

SUCCESS

</td>
<td>
Another listener on this channel has already responded.  Only the first respondent can continue the communication with the sender.

 If this HRESULT has an ERROR severity, the calling function should handle the error condition. 

</td>
</tr>
<tr>
<td>
CHANNEL_ALREADY_CLOSED

</td>
<td>
ERROR

or

SUCCESS

</td>
<td>
The channel has already closed. IPrintAsyncNotifyChannel::Release must not be called if this HRESULT is returned because the channel has already been closed and released.

 If this HRESULT has an ERROR severity, the calling function should handle the error condition. 

</td>
</tr>
<tr>
<td>CHANNEL_CLOSED_BY_ANOTHER_LISTENER</td>
<td>ERROR</td>
<td>A listening application, other than the caller, closed the communication channel. </td>
</tr>
<tr>
<td>CHANNEL_CLOSED_BY_SAME_LISTENER</td>
<td>ERROR</td>
<td>The caller has already closed the communication channel.</td>
</tr>
<tr>
<td>INVALID_NOTIFICATION_TYPE</td>
<td>ERROR</td>
<td>The specified notification type is invalid. </td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an HRESULT other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific HRESULT that was returned by the function, use the HRESULT_CODE macro. The following code example shows how these macros can be used.

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.


```cpp
if (SUCCEEDED(hr)) {
  // Call succeeded, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case CHANNEL_ACQUIRED:
      // Some action 
      break;
    case CHANNEL_ALREADY_CLOSED:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
} else {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case CHANNEL_CLOSED_BY_ANOTHER_LISTENER:
      // Some action 
      break;
    case CHANNEL_CLOSED_BY_SAME_LISTENER:
      // Some action 
      break;
    case INVALID_NOTIFICATION_TYPE:
      // Some action 
      break;
    case CHANNEL_ACQUIRED:
      // This can be an error and a successful return
      //  some action 
      break;
    case CHANNEL_ALREADY_CLOSED:
      // This can be an error and a successful return
      //  some action 
      break;
    default:
      // Default action 
      break;
  }
}

```

## -remarks

<b>CloseChannel</b> can be called by either side of the communication channel—the component that is hosted by the print spooler or the listening application.

If an <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification">IPrintAsyncNotifyChannel::SendNotification</a> call is made while the print spooler is processing an earlier call to <b>SendNotification</b>, the print spooler will queue the notifications. Queued notifications are discarded if either the component that is hosted by the print spooler or the application calls <b>CloseChannel</b>.

<b>CloseChannel</b> cannot be called immediately after the call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel">CreatePrintAsyncNotifyChannel</a>.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel">IPrintAsyncNotifyChannel</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>
