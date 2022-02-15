---
UID: NF:webservices.WsSendFaultMessageForError
title: WsSendFaultMessageForError function (webservices.h)
description: Sends a fault message given a WS_ERROR object.
helpviewer_keywords: ["WsSendFaultMessageForError","WsSendFaultMessageForError function [Web Services for Windows]","webservices/WsSendFaultMessageForError","wsw.wssendfaultmessageforerror"]
old-location: wsw\wssendfaultmessageforerror.htm
tech.root: wsw
ms.assetid: 1bb2af58-21c1-45e1-a685-91d200e9b452
ms.date: 12/05/2018
ms.keywords: WsSendFaultMessageForError, WsSendFaultMessageForError function [Web Services for Windows], webservices/WsSendFaultMessageForError, wsw.wssendfaultmessageforerror
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsSendFaultMessageForError
 - webservices/WsSendFaultMessageForError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsSendFaultMessageForError
---

# WsSendFaultMessageForError function


## -description

Sends a fault message given a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object.

## -parameters

### -param channel [in]

The channel to send the message on.

### -param replyMessage [in]

A message object to use to send the reply message.
                

The message object should be in <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a> or
                    <b>WS_MESSAGE_STATE_INITIALIZED</b>.  If an initialized message is provided,
                    it should have been initialized using <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_initialization">WS_FAULT_MESSAGE</a>.

### -param faultError [in]

The error object to use to construct the fault.

### -param faultErrorCode [in]

The error code associated with the fault.  This cannot
                    be a success code.
                

This error code is never included in the fault message directly, but 
                    instead is used as a fallback mechanism for creating a fault string in the case that
                    the <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object does not contain any error strings.

### -param faultDisclosure [in]

Controls how much of the error information is included in the fault message.

### -param requestMessage [in]

The request message.  This is used to obtain correlation information used
                    in formulating the reply message.
                

The message can be in any state but <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

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

The <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a> that is sent in the body of the message
                is constructed using the same rules as defined by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatefaultfromerror">WsCreateFaultFromError</a>.
            

The value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_ACTION_HEADER</a> used for
                the reply message is computed as follows:
            

<ul>
<li>If the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a> of the 
                channel is <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>, then no
                action is included in the message because the addressing
                version does not permit an action value for faults.
                </li>
<li>If the error object contains an action string (the
                length of the string returned by <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_error_property_id">WS_FAULT_ERROR_PROPERTY_ACTION</a> is greater than zero), then the action string is used.
                </li>
<li>If the error object does not contain an action, then 
                a default action value is supplied.
            </li>
</ul>
If the error object contains a header used to describe the
                fault as specified by <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_error_property_id">WS_FAULT_ERROR_PROPERTY_HEADER</a>,
                then the header is added to the headers of the fault message.
            

The fault message will include correlation information as appropriate
                to the <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION</a>.  See <a href="/windows/desktop/wsw/channel-layer-overview">Channel Layer Overview</a> for more information about correlating request reply messages.
            

If sending a fault without a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object, use
                <a href="/windows/desktop/api/webservices/nf-webservices-wssendreplymessage">WsSendReplyMessage</a>.
            

To add custom headers to the message, initialize the message <a href="/windows/desktop/api/webservices/nf-webservices-wsinitializemessage">WsInitializeMessage</a> with <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_initialization">WS_FAULT_MESSAGE</a> and then add the headers using 
                <a href="/windows/desktop/api/webservices/nf-webservices-wsaddcustomheader">WsAddCustomHeader</a> before calling this function.