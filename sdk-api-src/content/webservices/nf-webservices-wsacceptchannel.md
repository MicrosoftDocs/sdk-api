---
UID: NF:webservices.WsAcceptChannel
title: WsAcceptChannel function
author: windows-sdk-content
description: Accepts the next incoming message from the specified listener.
old-location: wsw\wsacceptchannel.htm
tech.root: wsw
ms.assetid: e18e0005-89bd-435e-9a12-6602c3c638b7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsAcceptChannel, WsAcceptChannel function [Web Services for Windows], webservices/WsAcceptChannel, wsw.wsacceptchannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsAcceptChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsAcceptChannel function


## -description



Accepts the next incoming message from the specified <a href="https://msdn.microsoft.com/fffda587-23f5-4c7a-93c5-f03d9d3fafb2">listener</a>.
            




## -parameters




### -param listener [in]

Pointer to a <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> structure representing the listener.
                This is the listener passed to <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>when the channel was created.
                




### -param channel [in]

Pointer to a <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> structure representing the channel to accept.
                


### -param asyncContext [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> data structure with information for invoking the function asynchronously.  Pass a <b>NULL</b> 
                 value for a synchronous operation.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
The listener or channel was aborted.
                
            

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OBJECT_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The listener has faulted. See the Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener or the channel or both were in an inappropriate state.
                
            See the Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The connection with the remote endpoint was terminated.


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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are  not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SECURITY_VERIFICATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Security verification was not successful for the received data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SECURITY_SYSTEM_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A security operation failed in the Windows Web Services framework.

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



Once you accept a channel, you must close it  when you no longer need it and free the resources by calling the  
                <a href="https://msdn.microsoft.com/e4928371-a172-4cc8-968b-12ae2ee2e0c6">WsCloseChannel</a> function, and then calling either the <a href="https://msdn.microsoft.com/74e36d19-c6db-4bba-90e3-88a48b6a1fb5">WsFreeChannel</a> or the <a href="https://msdn.microsoft.com/7aca8ae0-44a0-4ec7-87e8-bec9bd17d04b">WsResetChannel</a>.
            function. 

For <b>WsAcceptChannel</b> to succeed, the listener must be in WS_LISTENER_STATE_OPEN state, and the channel must be in WS_CHANNEL_STATE_CREATED state. For more information, see the <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> and <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE</a> enumerations.

If a listener is in the <b>WS_LISTENER_STATE_FAULTED</b> state,  
                <b>WsAcceptChannel</b> immediately returns the <b>WS_E_OBJECT_FAULTED</b> error code. If an
                application is calling <b>WsAcceptChannel</b> in a loop, the application must check for this
                error, so it can end the loop.



