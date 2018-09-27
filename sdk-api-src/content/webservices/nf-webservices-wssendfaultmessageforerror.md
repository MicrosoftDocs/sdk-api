---
UID: NF:webservices.WsSendFaultMessageForError
title: WsSendFaultMessageForError function
author: windows-sdk-content
description: Sends a fault message given a WS_ERROR object.
old-location: wsw\wssendfaultmessageforerror.htm
tech.root: wsw
ms.assetid: 1bb2af58-21c1-45e1-a685-91d200e9b452
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WsSendFaultMessageForError, WsSendFaultMessageForError function [Web Services for Windows], webservices/WsSendFaultMessageForError, wsw.wssendfaultmessageforerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WsSendFaultMessageForError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsSendFaultMessageForError function


## -description


Sends a fault message given a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object.
            


## -parameters




### -param channel [in]

The channel to send the message on.
                


### -param replyMessage [in]

A message object to use to send the reply message.
                

The message object should be in <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a> or
                    <b>WS_MESSAGE_STATE_INITIALIZED</b>.  If an initialized message is provided,
                    it should have been initialized using <a href="https://msdn.microsoft.com/f4a674c1-4017-49c8-aa9a-68f1d2b84378">WS_FAULT_MESSAGE</a>.
                


### -param faultError [in]

The error object to use to construct the fault.
                


### -param faultErrorCode [in]

The error code associated with the fault.  This cannot
                    be a success code.
                

This error code is never included in the fault message directly, but 
                    instead is used as a fallback mechanism for creating an fault string in the case that
                    the <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object does not contain any error strings.
                


### -param faultDisclosure [in]

Controls how much of the error information is included in the fault message.
                


### -param requestMessage [in]

The request message.  This is used to obtain correlation information used
                    in formulating the reply message.
                

The message can be in any state but <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
                


### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



This function can return one of these values.

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
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

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



The <a href="https://msdn.microsoft.com/7fe0b142-04a1-4a92-99ca-523412f7c94e">WS_FAULT</a> that is sent in the body of the message
                is constructed using the same rules as defined by <a href="https://msdn.microsoft.com/193854d7-3b7f-4f2b-b068-33b9c4d91e57">WsCreateFaultFromError</a>.
            

The value of the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_ACTION_HEADER</a> used for
                the reply message is computed as follows:
            

<ul>
<li>If the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a> of the 
                channel is <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>, then no
                action is included in the message because the addressing
                version does not permit an action value for faults.
                </li>
<li>If the error object contains an action string (the
                length of the string returned by <a href="https://msdn.microsoft.com/f5ae9ee9-18de-428d-9367-aa4a554577ea">WS_FAULT_ERROR_PROPERTY_ACTION</a>is greater than zero), then the action string is used.
                </li>
<li>If the error object does not contain an action, then 
                a default action value is supplied.
            </li>
</ul>
If the error object contains a header used to describe the
                fault as specified by <a href="https://msdn.microsoft.com/f5ae9ee9-18de-428d-9367-aa4a554577ea">WS_FAULT_ERROR_PROPERTY_HEADER</a>,
                then the header is added to the headers of the fault message.
            

The fault message will include correlation information as appropriate
                to the <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION</a>.  See <a href="https://msdn.microsoft.com/d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19">Channel Layer Overview</a>for more information about correlating request reply messages.
            

If sending a fault without a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object, use
                <a href="https://msdn.microsoft.com/cabfd07b-294c-4e3a-9d50-84d9b4d98f62">WsSendReplyMessage</a>.
            

To add custom headers to the message, initialize the message <a href="https://msdn.microsoft.com/26eafc5f-6636-4f96-a037-7935cdac5900">WsInitializeMessage</a>with <a href="https://msdn.microsoft.com/f4a674c1-4017-49c8-aa9a-68f1d2b84378">WS_FAULT_MESSAGE</a> and then add the headers using 
                <a href="https://msdn.microsoft.com/4b95085a-e522-4ab2-b7c9-d332599c5598">WsAddCustomHeader</a> before calling this function.
            



