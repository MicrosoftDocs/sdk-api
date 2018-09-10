---
UID: NF:prnasnot.IPrintAsyncNotifyChannel.CloseChannel
title: IPrintAsyncNotifyChannel::CloseChannel
author: windows-sdk-content
description: Closes the channel.
old-location: gdi\iprintasyncnotifychannel_iprintasyncnotifychannel__closechannel.htm
tech.root: printdocs
ms.assetid: d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CloseChannel, CloseChannel method [Windows GDI], CloseChannel method [Windows GDI],IPrintAsyncNotifyChannel interface, IPrintAsyncNotifyChannel interface [Windows GDI],CloseChannel method, IPrintAsyncNotifyChannel.CloseChannel, IPrintAsyncNotifyChannel::CloseChannel, _win32_IPrintAsyncNotifyChannel_CloseChannel, gdi.iprintasyncnotifychannel_iprintasyncnotifychannel__closechannel, prnasnot/IPrintAsyncNotifyChannel::CloseChannel
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
 - IPrintAsyncNotifyChannel.CloseChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa376932(v=VS.85).aspx">Error Handling</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr)) {
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
</pre>
</td>
</tr>
</table></span></div>



## -remarks



<b>CloseChannel</b> can be called by either side of the communication channel—the component that is hosted by the print spooler or the listening application.

If an <a href="https://msdn.microsoft.com/729286d4-75ee-441e-b63d-fef72d41533a">IPrintAsyncNotifyChannel::SendNotification</a> call is made while the print spooler is processing an earlier call to <b>SendNotification</b>, the print spooler will queue the notifications. Queued notifications are discarded if either the component that is hosted by the print spooler or the application calls <b>CloseChannel</b>.

<b>CloseChannel</b> cannot be called immediately after the call to <a href="https://msdn.microsoft.com/52cc586a-a565-46c6-b1b7-8613ad111ed3">CreatePrintAsyncNotifyChannel</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/8973cf5a-bbce-43c2-b418-2807842d43c0">IPrintAsyncNotifyChannel</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

