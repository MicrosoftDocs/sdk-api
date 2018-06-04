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

# UnRegisterForPrintAsyncNotifications function


## -description


Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.


## -parameters




### -param Arg1

TBD




#### - hRegistrationHandler [in]

The registration handle to be unregistered.


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
<td>ALREADY_UNREGISTERED</td>
<td>
SUCCESS

ERROR

</td>
<td>The registration handler has already been unregistered. If this HRESULT has an ERROR severity, the calling function should handle the error condition.</td>
</tr>
<tr>
<td>NOT_REGISTERED</td>
<td>SUCCESS</td>
<td>The registration handler was not registered.</td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an <b>HRESULT</b> other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific <b>HRESULT</b> that was returned by the function, use the HRESULT_CODE macro.

The following code example shows how these macros can be used to evaluate the return value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr)) {
  // Call succeeded, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case S_OK:
      // Some action 
      break;
    case NOT_REGISTERED:
      // Some action 
      break;
    case ALREADY_UNREGISTERED:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
} else {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    // This can be error and a successful return
    case ALREADY_UNREGISTERED:
      // Some action 
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
For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.

See <a href="https://msdn.microsoft.com/2fb6698c-5d59-4ba0-a8ff-1313fade438c">PrintAsyncNotifyError</a> for other possible return values.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
A call to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a> must return <i>hRegistrationHandler</i>.

If the channel is bidirectional, a call to <b>UnRegisterForPrintAsyncNotifications</b> only prevents notifications from communication channels created after that point. To end notifications from the existing channel, the listening application must close the channel with <a href="https://msdn.microsoft.com/d5878cf1-c2c3-4f33-bc08-e4f868c8a5e7">IPrintAsyncNotifyChannel::CloseChannel</a>.

A call to <b>UnRegisterForPrintAsyncNotifications</b> will decrement the reference count of the <i>pCallback</i> object passed to <a href="https://msdn.microsoft.com/f5a01819-75d0-42a0-b66f-5a25a48b091c">RegisterForPrintAsyncNotifications</a>.

After this function succeeds, <i>hRegistrationHandler</i> is invalid and must not be used again.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

