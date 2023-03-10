---
UID: NF:webservices.WsRequestReply
title: WsRequestReply function (webservices.h)
description: Used to send a request message and receive a correlated reply message.
helpviewer_keywords: ["WsRequestReply","WsRequestReply function [Web Services for Windows]","webservices/WsRequestReply","wsw.wsrequestreply"]
old-location: wsw\wsrequestreply.htm
tech.root: wsw
ms.assetid: 681e9c1c-bb18-4ffa-9287-e1965274043b
ms.date: 12/05/2018
ms.keywords: WsRequestReply, WsRequestReply function [Web Services for Windows], webservices/WsRequestReply, wsw.wsrequestreply
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
 - WsRequestReply
 - webservices/WsRequestReply
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
 - WsRequestReply
---

# WsRequestReply function


## -description

Used to send a request message and receive a correlated reply message.

## -parameters

### -param channel [in]

The channel to do the request-reply operation on.

### -param requestMessage [in]

The message object to use to send the request.
                

The message object should be in <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a> or
                    <b>WS_MESSAGE_STATE_INITIALIZED</b>.

### -param requestMessageDescription [in]

The action field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> is used as the
                    action header for the request message.  This field may be <b>NULL</b> if no action
                    is required.
                

The bodyElementDescription field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> is used to serialize the body of the request message.  This field may be 
                    <b>NULL</b> if no body element is desired.  See <a href="/windows/desktop/api/webservices/nf-webservices-wswritebody">WsWriteBody</a> for
                    information about how the body is serialized according to the bodyElementDescription.

### -param writeOption [in]

Whether the body element is required, and how the value is allocated.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for more information.

### -param requestBodyValue

A pointer to the value to serialize in the body of the request object.

### -param requestBodyValueSize [in]

The size of the request value being serialized, in bytes.

### -param replyMessage [in]

The message object to use to receive the reply.
                

The message object should be in <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

### -param replyMessageDescription [in]

The action field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> is used to verify
                    the action header of the received reply message.  This field may be <b>NULL</b> if no action
                    is required.  If <b>NULL</b>, the action header of the received message is ignored
                    if present.
                

The bodyElementDescription field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> is used to deserialize the body of the reply message.  This field may be 
                    <b>NULL</b> if no body element is desired.  See <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbody">WsReadBody</a> for 
                    information about how the body is deserialized according to the bodyElementDescription.

### -param readOption [in]

Whether the reply body element is required, and how to allocate the value.                    For more information, see <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbody">WsReadBody</a>.

### -param heap [in, optional]

The heap used to allocate deserialized reply body values.
                    If the heap is not necessary for the given type, then this
                    parameter can be <b>NULL</b>.

### -param value

Where to store the deserialized values of the body.
                

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.
                

If the bodyElementDescription of the reply <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> 
                    is <b>NULL</b>, then this parameter is not touched.  In this case, the
                    parameter does not need to be specified.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

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
<dt><b>WS_E_ENDPOINT_FAULT_RECEIVED</b></dt>
</dl>
</td>
<td width="60%">
The reply message contained a fault.  The fault can be extracted from the
                    <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> using <a href="/windows/desktop/api/webservices/nf-webservices-wsgeterrorproperty">WsGetErrorProperty</a>.
                

</td>
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
<dt><b>WS_E_ENDPOINT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint does not exist or could not be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access was denied by the remote endpoint.

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
<dt><b>WS_E_ENDPOINT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint could not process the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint is not currently in service at this location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_TOO_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint is unable to process the request due to being overloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint was not reachable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_ENDPOINT_URL</b></dt>
</dl>
</td>
<td width="60%">
The endpoint address URL is invalid.

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
<dt><b>WS_E_PROXY_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access was denied by the HTTP proxy server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server could not process the request.

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
<dt><b>WS_E_PROXY_REQUIRES_BASIC_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'basic'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_DIGEST_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'digest'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_NEGOTIATE_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'negotiate'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_NTLM_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'NTLM'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_BASIC_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'basic'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_DIGEST_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'digest'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_NEGOTIATE_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'negotiate'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_NTLM_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'NTLM'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_E_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
A required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_E_CN_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
The certificates CN name does not match the passed value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_E_UNTRUSTEDROOT</b></dt>
</dl>
</td>
<td width="60%">
A certificate chain processed, but terminated in a root certificate which is not trusted by the trust provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_E_WRONG_USAGE</b></dt>
</dl>
</td>
<td width="60%">
The certificate is not valid for the requested usage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_REVOCATION_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The revocation function was unable to check revocation because the revocation server was offline.

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

The messages are correlated as appropriate to the <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION</a>.
                See <a href="/windows/desktop/wsw/channel-layer-overview">Channel Layer Overview</a> for more information about correlating
                request reply messages.