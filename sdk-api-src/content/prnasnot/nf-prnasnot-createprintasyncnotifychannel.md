---
UID: NF:prnasnot.CreatePrintAsyncNotifyChannel
title: CreatePrintAsyncNotifyChannel function (prnasnot.h)
description: Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.
helpviewer_keywords: ["CreatePrintAsyncNotifyChannel","CreatePrintAsyncNotifyChannel function [Windows GDI]","_win32_CreatePrintAsyncNotifyChannel","gdi.createprintasyncnotifychannel","prnasnot/CreatePrintAsyncNotifyChannel"]
old-location: gdi\createprintasyncnotifychannel.htm
tech.root: xps
ms.assetid: 52cc586a-a565-46c6-b1b7-8613ad111ed3
ms.date: 12/05/2018
ms.keywords: CreatePrintAsyncNotifyChannel, CreatePrintAsyncNotifyChannel function [Windows GDI], _win32_CreatePrintAsyncNotifyChannel, gdi.createprintasyncnotifychannel, prnasnot/CreatePrintAsyncNotifyChannel
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
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreatePrintAsyncNotifyChannel
 - prnasnot/CreatePrintAsyncNotifyChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Spoolss.dll
api_name:
 - CreatePrintAsyncNotifyChannel
---

# CreatePrintAsyncNotifyChannel function


## -description

Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.

## -parameters

### -param pszName [in]

A pointer to the name of a print server or print queue.

### -param pNotificationType [in]

A pointer to the GUID of the data schema for the type of notifications to be sent in the channel.

### -param eUserFilter [in]

A value specifying whether notifications will be sent to:

<ul>
<li>Only applications that are running as the same user as the Print Spooler-hosted plug-in sender.</li>
<li>A broader set of listening applications.</li>
</ul>

### -param eConversationStyle [in]

A value specifying whether communication is bidirectional or unidirectional.

### -param pCallback [in]

A pointer to an object that the listening application will use to call back the Print Spooler-hosted component. This should be <b>NULL</b> if <i>directionality</i> is <b>kUniDirectional</b>.

### -param ppIAsynchNotification [out]

A pointer to the new channel.

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
<td>CHANNEL_ALREADY_OPENED</td>
<td>ERROR</td>
<td>The channel has already been opened.</td>
</tr>
<tr>
<td>MAX_CHANNEL_COUNT_EXCEEDED</td>
<td>ERROR</td>
<td>The maximum number of listening applications have already registered for the specified type of notification with the specified queue or print server. The default maximum is 10,000.</td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an <b>HRESULT</b> other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific <b>HRESULT</b> that was returned by the function, use the HRESULT_CODE macro.

The following code example shows how these macros can be used to evaluate the return value.


```cpp
if (SUCCEEDED(hr)){
  //Call was successful 
}

if (FAILED(hr)) {
  // Call failed 
}

if (FAILED(hr)) {
  // Call failed 
  switch (HRESULT_CODE(hr)){
    case CHANNEL_ALREADY_OPENED:
      // Some action 
      break;
    case MAX_CHANNEL_COUNT_EXCEEDED:
      // Some action 
      break;
    default:
      //Default action 
      break;
  }
} else {
  //call succeeded 
}

```


For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
A component can open a channel only if it runs in the Print Spooler's process. For example, if an application loads a printer driver, the driver cannot open a channel, but a printer driver loaded inside the Print Spooler can open a channel. Listening applications can either be inside or outside the Print Spooler's process.

To close a channel, call <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a>; however, <b>IPrintAsyncNotifyChannel::CloseChannel</b> cannot be called immediately after the call to <b>CreatePrintAsyncNotifyChannel</b>.

Call IPrintAsyncNotifyChannel::Release() only:

<ol>
<li>if it is an explicit match to an earlier IPrintAsyncNotifyChannel::AddRef() call.</li>
<li>if the channel is a UniDirectional channel and you are abandoning the pointer received in a successful call to CreatePrintAsyncNotifyChannel.</li>
<li>if, after you created a BiDirectional channel or in the implementation of IPrintNotifyAsyncCallback::OnEventNotify and:<ol>
<li>you did not call IPrintAsyncNotifyChannel::SendNotification or IPrintAsyncNotifyChannel::CloseChannel OR</li>
<li>you did not retry a call to IPrintAsyncNotifyChannel::SendNotification or IPrintAsyncNotifyChannel::CloseChannel that failed OR</li>
<li>on the server side, you didn't retry a call to IPrintAsyncNotifyChannel::SendNotification that succeeded with the return value NO_LISTENER OR</li>
<li>on the client side, you didn't retry a call to IPrintAsyncNotifyChannel::SendNotification that succeeded with return value CHANNEL_ACQUIRED.</li>
</ol>
</li>
</ol>

## -see-also

<a href="/windows/desktop/SecAuthZ/client-impersonation">Client Impersonation</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>