---
UID: NF:prnasnot.IPrintAsyncNotifyCallback.ChannelClosed
title: IPrintAsyncNotifyCallback::ChannelClosed
author: windows-sdk-content
description: Advises one member of a communication channel to notify the other member that the channel is being closed.
old-location: gdi\iprintasyncnotifycallback_iprintasyncnotifycallback__channelclosed.htm
old-project: printdocs
ms.assetid: 245f4d86-a6b9-421a-add5-fb7afbbacb45
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ChannelClosed, ChannelClosed method [Windows GDI], ChannelClosed method [Windows GDI],IPrintAsyncNotifyCallback interface, IPrintAsyncNotifyCallback interface [Windows GDI],ChannelClosed method, IPrintAsyncNotifyCallback.ChannelClosed, IPrintAsyncNotifyCallback::ChannelClosed, _win32_IPrintAsyncNotifyCallback_ChannelClosed, gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__channelclosed, prnasnot/IPrintAsyncNotifyCallback::ChannelClosed
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PrintAsyncNotifyUserFilter
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyCallback.ChannelClosed
product: Windows
targetos: Windows
req.lib: 
req.dll: Prnasnot.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPrintAsyncNotifyCallback::ChannelClosed


## -description


Advises one member of a communication channel to notify the other member that the channel is being closed.


## -parameters




### -param pChannel [in]

A pointer to the channel used by the sender and the listener.


### -param pData [in]

A pointer to the object that contains the notification data or response.


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
<td>This function completed successfully.</td>
</tr>
<tr>
<td>CHANNEL_ALREADY_CLOSED</td>
<td>ERROR</td>
<td>The channel has already been closed.</td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an HRESULT other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific HRESULT that was returned by the function, use the HRESULT_CODE macro.

See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for other possible return values.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.

The following code example shows how these macros can be used to evaluate the return value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
if (SUCCEEDED(hr)){
  // Call was successful 
}

if (FAILED(hr)) {
  // Call failed 
}

if (FAILED(hr)) {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case CHANNEL_ALREADY_CLOSED:
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



When a component that is hosted by the print spooler closes a communication channel with a listening application, the component should call the <b>ChannelClosed</b> method of the <a href="https://msdn.microsoft.com/e2b021cd-1cfd-42b7-b6e4-7f8671b013f6">IPrintAsyncNotifyCallback</a> object, which the listening application provided at the time it registered for notifications. If the print server crashes, the print spooler will attempt to call the <a href="https://msdn.microsoft.com/2f398173-3cd6-46da-931d-057d1dccbe9b">OnEventNotify</a> method of the <b>IPrintAsyncNotifyCallback</b> object provided by the listening application. It will send a notification of type NOTIFICATION_RELEASE.

If the listening application closes a bidirectional communication channel, it should call the <b>ChannelClosed</b> method of the <a href="https://msdn.microsoft.com/e2b021cd-1cfd-42b7-b6e4-7f8671b013f6">IPrintAsyncNotifyCallback</a> object provided by the component when it created the channel. If the listening application crashes, the print spooler will call the <a href="https://msdn.microsoft.com/2f398173-3cd6-46da-931d-057d1dccbe9b">OnEventNotify</a> method of the <b>IPrintAsyncNotifyCallback</b> object provided by the  component that is hosted by the print spooler. It will send a notification of type NOTIFICATION_RELEASE.




## -see-also




<a href="https://msdn.microsoft.com/e96c957f-3972-4afc-9d76-a4725b8688f8">Asynchronous Printing Notification Interfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>



<a href="https://msdn.microsoft.com/e2b021cd-1cfd-42b7-b6e4-7f8671b013f6">IPrintAsyncNotifyCallback</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

