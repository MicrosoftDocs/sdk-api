---
UID: NC:webservices.WS_CLOSE_LISTENER_CALLBACK
title: WS_CLOSE_LISTENER_CALLBACK
author: windows-sdk-content
description: Handles the WsCloseListener call for a WS_CUSTOM_CHANNEL_BINDING.
old-location: wsw\ws_close_listener_callback.htm
tech.root: wsw
ms.assetid: 9a5d6b10-b4c8-41ba-9b69-4537e44416df
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_CLOSE_LISTENER_CALLBACK, WS_CLOSE_LISTENER_CALLBACK callback, WS_CLOSE_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_CLOSE_LISTENER_CALLBACK, wsw.ws_close_listener_callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_CLOSE_LISTENER_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_CLOSE_LISTENER_CALLBACK callback function


## -description


Handles the <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a> call
                for a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
            


## -parameters




### -param *listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                


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
The close was aborted by a call to <a href="https://msdn.microsoft.com/894a325b-53ac-4f45-ac24-87ed3a40b03d">WsAbortListener</a> as it was closing.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener was in an inappropriate state.
                

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



See <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a> for information about the contract
                of this API.
            



