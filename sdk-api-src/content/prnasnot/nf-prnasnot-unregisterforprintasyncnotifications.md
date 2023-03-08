---
UID: NF:prnasnot.UnRegisterForPrintAsyncNotifications
title: UnRegisterForPrintAsyncNotifications function (prnasnot.h)
description: Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.
helpviewer_keywords: ["UnRegisterForPrintAsyncNotifications","UnRegisterForPrintAsyncNotifications function [Windows GDI]","_win32_UnRegisterForPrintAsyncNotifications","gdi.unregisterforprintasyncnotifications","prnasnot/UnRegisterForPrintAsyncNotifications"]
old-location: gdi\unregisterforprintasyncnotifications.htm
tech.root: xps
ms.assetid: 2b039018-71c0-4110-8c0b-702927f58df4
ms.date: 12/05/2018
ms.keywords: UnRegisterForPrintAsyncNotifications, UnRegisterForPrintAsyncNotifications function [Windows GDI], _win32_UnRegisterForPrintAsyncNotifications, gdi.unregisterforprintasyncnotifications, prnasnot/UnRegisterForPrintAsyncNotifications
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
 - UnRegisterForPrintAsyncNotifications
 - prnasnot/UnRegisterForPrintAsyncNotifications
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
 - UnRegisterForPrintAsyncNotifications
---

# UnRegisterForPrintAsyncNotifications function


## -description

Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.

## -parameters

### -param unnamedParam1 [in]

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


```cpp
if (SUCCEEDED(hr)) {
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

```


For more information about COM error codes, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

See <a href="/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for other possible return values.

## -remarks

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
A call to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications">RegisterForPrintAsyncNotifications</a> must return <i>hRegistrationHandler</i>.

If the channel is bidirectional, a call to <b>UnRegisterForPrintAsyncNotifications</b> only prevents notifications from communication channels created after that point. To end notifications from the existing channel, the listening application must close the channel with <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel">IPrintAsyncNotifyChannel::CloseChannel</a>.

A call to <b>UnRegisterForPrintAsyncNotifications</b> will decrement the reference count of the <i>pCallback</i> object passed to <a href="/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications">RegisterForPrintAsyncNotifications</a>.

After this function succeeds, <i>hRegistrationHandler</i> is invalid and must not be used again.

## -see-also

<a href="/windows/desktop/printdocs/printing-and-print-spooler-functions">Print Spooler API Functions</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>