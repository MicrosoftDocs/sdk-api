---
UID: NF:webservices.WsSendReplyMessage
title: WsSendReplyMessage function (webservices.h)
description: Sends a message which is a reply to a received message.
helpviewer_keywords: ["WsSendReplyMessage","WsSendReplyMessage function [Web Services for Windows]","webservices/WsSendReplyMessage","wsw.wssendreplymessage"]
old-location: wsw\wssendreplymessage.htm
tech.root: wsw
ms.assetid: cabfd07b-294c-4e3a-9d50-84d9b4d98f62
ms.date: 12/05/2018
ms.keywords: WsSendReplyMessage, WsSendReplyMessage function [Web Services for Windows], webservices/WsSendReplyMessage, wsw.wssendreplymessage
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
 - WsSendReplyMessage
 - webservices/WsSendReplyMessage
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
 - WsSendReplyMessage
---

# WsSendReplyMessage function


## -description

Sends a message which is a reply to a received message.

## -parameters

### -param channel [in]

A pointer to the <b>Channel</b> object on which to send the reply Message.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> object.

### -param replyMessage [in]

A pointer to the <b>Message</b> object for sending the reply.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.
                
Message object state must be set to <b>WS_MESSAGE_STATE_EMPTY</b>  or <b>WS_MESSAGE_STATE_INITIALIZED</b>.

<div class="alert"><b>Note</b>  If an initialized message is provided it must be initialized using <b>WS_REPLY_MESSAGE</b> or <b>WS_FAULT_MESSAGE</b>.
</div>
<div> </div>

### -param replyMessageDescription [in]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> object.  The <b>action</b> field of <b>WS_MESSAGE_DESCRIPTION</b> is used as the <b>action</b> header for the reply message.  This field can be <b>NULL</b> if no action is required.
                

The <b>bodyElementDescription</b>  field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> is used to serialize the body of the reply message.  This field may be <b>NULL</b> if no body element is desired.  See <a href="/windows/desktop/api/webservices/nf-webservices-wswritebody">WsWriteBody</a> for information about how the <b>bodyElementDescription</b> is used to serialize a value.

### -param writeOption [in]

Determines whether the body element is required, and how the value is allocated.

See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.

### -param replyBodyValue

A void pointer to the value to serialize in the reply message.

### -param replyBodyValueSize [in]

The size  in bytes of the reply value being serialized.

### -param requestMessage [in]

A pointer to a WS_MESSAGE object encapsulating the request message text.  This is used to obtain correlation information used in formulating the reply message.

<div class="alert"><b>Note</b>  The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b>.
</div>
<div> </div>

### -param asyncContext [in, optional]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> data structure with information about invoking the function asynchronously.  A <b>NULL</b> value indicates a request for synchronous operation.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

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
<dt><b>WS_E_SECURITY_TOKEN_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
A security token was rejected by the server because it has expired.

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

The reply message will including correlation information as appropriate 
                to the <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION</a>.  See <a href="/windows/desktop/wsw/channel-layer-overview">Channel Layer Overview</a> 
                for more information about correlating request reply messages.