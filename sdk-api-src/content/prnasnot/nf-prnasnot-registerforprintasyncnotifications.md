---
UID: NF:prnasnot.RegisterForPrintAsyncNotifications
title: RegisterForPrintAsyncNotifications function (prnasnot.h)
description: Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.
helpviewer_keywords: ["RegisterForPrintAsyncNotifications","RegisterForPrintAsyncNotifications function [Windows GDI]","_win32_RegisterForPrintAsyncNotifications","gdi.registerforprintasyncnotifications","prnasnot/RegisterForPrintAsyncNotifications"]
old-location: gdi\registerforprintasyncnotifications.htm
tech.root: xps
ms.assetid: f5a01819-75d0-42a0-b66f-5a25a48b091c
ms.date: 12/05/2018
ms.keywords: RegisterForPrintAsyncNotifications, RegisterForPrintAsyncNotifications function [Windows GDI], _win32_RegisterForPrintAsyncNotifications, gdi.registerforprintasyncnotifications, prnasnot/RegisterForPrintAsyncNotifications
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
req.lib: WinSpool.lib
req.dll: Spoolss.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterForPrintAsyncNotifications
 - prnasnot/RegisterForPrintAsyncNotifications
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
 - RegisterForPrintAsyncNotifications
---

# RegisterForPrintAsyncNotifications function


## -description

Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.

## -parameters

### -param pszName [in]

A pointer to the name of a print server or print queue.

### -param pNotificationType [in]

A pointer to the GUID of the data schema for the type of notifications that the application must receive.

### -param eUserFilter [in]

A value specifying whether notifications will be sent to:

<ul>
<li>Only applications that are running as the same user as the Print Spooler-hosted plug-in sender.</li>
<li>A broader set of listening applications.</li>
</ul>

### -param eConversationStyle [in]

A value specifying whether communication is bidirectional or unidirectional.

### -param pCallback [in]

A pointer to an object that the Print Spooler-hosted component will use to call back the application. This should never be <b>NULL</b>.

### -param phNotify [out]

A pointer to a structure that represents the registration.

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
<td>ALREADY_REGISTERED</td>
<td>ERROR</td>
<td>The registration object has already been registered.</td>
</tr>
<tr>
<td>LOCAL_ONLY_REGISTRATION</td>
<td>SUCCESS</td>
<td>Registration for local notification was successful. Registration for remote notifications was not.</td>
</tr>
<tr>
<td>MAX_REGISTRATION_COUNT_EXCEEDED</td>
<td>ERROR</td>
<td>The maximum number of registrations has been reached. No more registrations are permitted.</td>
</tr>
<tr>
<td>REMOTE_ONLY_REGISTRATION</td>
<td>SUCCESS</td>
<td>Registration for remote notifications was successful. Registration for local notifications was not.</td>
</tr>
</table>
 

The return values are COM error codes. Because this function might complete the operation successfully yet return an HRESULT other than S_OK you should use the SUCCEEDED or FAILED macro to determine the success of the call. To get the specific HRESULT that was returned by the function, use the HRESULT_CODE macro.

The following code example shows how these macros can be used to evaluate the return value.


```cpp
if (SUCCEEDED(hr)) {
  // Call succeeded, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case S_OK:
      // Some action 
      break;
      case LOCAL_ONLY_REGISTRATION:
      // Some action 
      break;
    case REMOTE_ONLY_REGISTRATION:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
} else {
  // Call failed, check HRESULT value returned
  switch (HRESULT_CODE(hr)){
    case ALREADY_REGISTERED:
      // Some action 
      break;
    case MAX_REGISTRATION_COUNT_EXCEEDED:
      // Some action 
      break;
    default:
      // Default action 
      break;
  }
}

```


For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
To stop notifications through a unidirectional channel, the listening application passes the <i>pRegistrationHandler</i> value returned by <b>RegisterForPrintAsyncNotifications</b> to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications">UnRegisterForPrintAsyncNotifications</a>. For a bidirectional channel, call <b>UnRegisterForPrintAsyncNotifications</b> to block notifications in any new channels that were created after that call. To block notifications on existing bidirectional channels, the listening application must close the channel with <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a>.

As a result of a <b>RegisterForPrintAsyncNotifications</b> call, the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> method is called for the <i>pCallback</i> object. Calling <a href="/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications">UnRegisterForPrintAsyncNotifications</a> will release the <i>pCallback</i> object. The reference count of <i>pCallback</i> object will be also incremented when a channel is created and decremented when the channel is closed.

The <i>pSchema</i> parameter is a GUID pointer that the spooler accepts and uses to filter the listener clients. Any client of the spooler asynchronous notification mechanism can define its own notification type. Even though the spooler is unaware of the notification type that is sent, it still filters the listener clients based on the notification type. The notification schema that <i>pSchema</i> references is the schema that is used by the notification object that exposes <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a>. Clients of the spooler notification pipe can define their own data schema and can send any data type back and forth and the GUID referenced by <i>pSchema</i> is unique to that data schema.

## -see-also

<a href="/windows/desktop/SecAuthZ/client-impersonation">Client Impersonation</a>



<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>