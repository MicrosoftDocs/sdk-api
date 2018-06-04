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
 

 

