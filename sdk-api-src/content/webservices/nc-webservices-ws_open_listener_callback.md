---
UID: NC:webservices.WS_OPEN_LISTENER_CALLBACK
title: WS_OPEN_LISTENER_CALLBACK
author: windows-sdk-content
description: Handles the WsOpenListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_open_listener_callback.htm
old-project: wsw
ms.assetid: 061111f5-a568-4a8a-9892-9c8a352556ef
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_OPEN_LISTENER_CALLBACK, WS_OPEN_LISTENER_CALLBACK callback, WS_OPEN_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_OPEN_LISTENER_CALLBACK, wsw.ws_open_listener_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_OPEN_LISTENER_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_OPEN_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                


### -param *url [in]

The URL to listen on.  The format and interpretation of the URL
                    is defined by the custom listener.
                


### -param *asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
                


### -param *error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The listener was aborted during the open, or before the open.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener is in the incorrect state.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The address is already being used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The address is not valid for this context.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The operation did not complete within the time allotted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



See <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> for information about the contract
                of this API.
            



