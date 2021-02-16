---
UID: NF:prnasnot.IPrintAsyncNotifyCallback.ChannelClosed
title: IPrintAsyncNotifyCallback::ChannelClosed (prnasnot.h)
description: Advises one member of a communication channel to notify the other member that the channel is being closed.
helpviewer_keywords: ["ChannelClosed","ChannelClosed method [Windows GDI]","ChannelClosed method [Windows GDI]","IPrintAsyncNotifyCallback interface","IPrintAsyncNotifyCallback interface [Windows GDI]","ChannelClosed method","IPrintAsyncNotifyCallback.ChannelClosed","IPrintAsyncNotifyCallback::ChannelClosed","_win32_IPrintAsyncNotifyCallback_ChannelClosed","gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__channelclosed","prnasnot/IPrintAsyncNotifyCallback::ChannelClosed"]
old-location: gdi\iprintasyncnotifycallback_iprintasyncnotifycallback__channelclosed.htm
tech.root: xps
ms.assetid: 245f4d86-a6b9-421a-add5-fb7afbbacb45
ms.date: 12/05/2018
ms.keywords: ChannelClosed, ChannelClosed method [Windows GDI], ChannelClosed method [Windows GDI],IPrintAsyncNotifyCallback interface, IPrintAsyncNotifyCallback interface [Windows GDI],ChannelClosed method, IPrintAsyncNotifyCallback.ChannelClosed, IPrintAsyncNotifyCallback::ChannelClosed, _win32_IPrintAsyncNotifyCallback_ChannelClosed, gdi.iprintasyncnotifycallback_iprintasyncnotifycallback__channelclosed, prnasnot/IPrintAsyncNotifyCallback::ChannelClosed
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
 - IPrintAsyncNotifyCallback::ChannelClosed
 - prnasnot/IPrintAsyncNotifyCallback::ChannelClosed
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
 - IPrintAsyncNotifyCallback.ChannelClosed
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

```

## -remarks

When a component that is hosted by the print spooler closes a communication channel with a listening application, the component should call the <b>ChannelClosed</b> method of the <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback">IPrintAsyncNotifyCallback</a> object, which the listening application provided at the time it registered for notifications. If the print server crashes, the print spooler will attempt to call the <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify">OnEventNotify</a> method of the <b>IPrintAsyncNotifyCallback</b> object provided by the listening application. It will send a notification of type NOTIFICATION_RELEASE.

If the listening application closes a bidirectional communication channel, it should call the <b>ChannelClosed</b> method of the <a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback">IPrintAsyncNotifyCallback</a> object provided by the component when it created the channel. If the listening application crashes, the print spooler will call the <a href="/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify">OnEventNotify</a> method of the <b>IPrintAsyncNotifyCallback</b> object provided by the  component that is hosted by the print spooler. It will send a notification of type NOTIFICATION_RELEASE.

## -see-also

<a href="/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>



<a href="/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback">IPrintAsyncNotifyCallback</a>



<a href="/windows/desktop/printdocs/printdocs-printing">Printing</a>