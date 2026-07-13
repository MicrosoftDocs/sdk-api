---
UID: NF:webservices.WsReceiveMessage
title: WsReceiveMessage function (webservices.h)
description: Receive a message and deserialize the body of the message as a value.
helpviewer_keywords: ["WsReceiveMessage","WsReceiveMessage function [Web Services for Windows]","webservices/WsReceiveMessage","wsw.wsreceivemessage"]
old-location: wsw\wsreceivemessage.htm
tech.root: wsw
ms.assetid: 3976c02c-d052-4eae-b675-edd317ac6464
ms.date: 12/05/2018
ms.keywords: WsReceiveMessage, WsReceiveMessage function [Web Services for Windows], webservices/WsReceiveMessage, wsw.wsreceivemessage
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
 - WsReceiveMessage
 - webservices/WsReceiveMessage
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
 - WsReceiveMessage
---

# WsReceiveMessage function


## -description

Receive a message and deserialize the body of the message as a value.

## -parameters

### -param channel [in]

The channel to receive from.

### -param message [in]

The message object used to receive.
                

The message should be in <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a> state.

### -param messageDescriptions

An array of pointers to message descriptions that specifies the metadata for
                    the expected types of messages.

### -param messageDescriptionCount [in]

The number of items in the messageDescriptions array.

### -param receiveOption [in]

Whether the message is required.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_receive_option">WS_RECEIVE_OPTION</a> for more information.

### -param readBodyOption [in]

Whether the body element is required, and how to allocate the value.  
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.

### -param heap [in, optional]

The heap to store the deserialized values in.  If the heap is 
                    not required for the given type, then this parameter can be <b>NULL</b>.

### -param value

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.
                

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_receive_option">WS_RECEIVE_OPTIONAL_MESSAGE</a> is specified for the receiveOption
                    parameter, and no more messages are available on the channel, 
                    this parameter is not touched.  In this case, the function returns <b>WS_S_END</b>.
                (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

If the bodyElementDescription of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> that
                    matched is <b>NULL</b>, then this parameter is not touched.  In this case, the
                    parameter does not need to be specified.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param index

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_receive_option">WS_RECEIVE_OPTIONAL_MESSAGE</a> is specified for the receiveOption
                    parameter, and no more messages are available on the channel, 
                    this parameter is untouched.  In this case, the function will
                    return <b>WS_S_END</b>.
                

Otherwise, if the function succeeds this will contain the zero-based 
                    index into the array of message descriptions indicating which one matched.
                

This parameter may be <b>NULL</b> if the caller is not interested in the value
                    (for example, if there is only one message description).

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
<dt><b>WS_S_END</b></dt>
</dl>
</td>
<td width="60%">
The receive option <a href="/windows/desktop/api/webservices/ne-webservices-ws_receive_option">WS_RECEIVE_OPTIONAL_MESSAGE</a> was specified and
                    there are no more messages available for the channel.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_FAULT_RECEIVED</b></dt>
</dl>
</td>
<td width="60%">
The received message contained a fault.  The fault can be extracted from the 
                    <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> using <a href="/windows/desktop/api/webservices/nf-webservices-wsgeterrorproperty">WsGetErrorProperty</a>.
                

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

This function uses metadata about the expected message types in order to deserialize the body.  
                The metadata is an array of pointers to <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a>s.
                Each message description contains an action value, which is used to match against
                the action of the message, and an <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> which provides the metadata for the body element.
            

When the message headers have been received, the function will scan the array
                in order to find a match against the action.  The first message description
                that matches is used to deserialize the body, and the zero-based index 
                of this message description in the array is returned in the index out parameter.
                If the function succeeds, the index out parameter will always be set to indicate which
                message description was used.
            

In order for a message description to match, the action value must match that of
                the message exactly.  If the action in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> 
                is <b>NULL</b>, then the action always matches.  This can be used in the case where there 
                is no action header in the received message, or if the body is always the same no matter 
                what the action is.
            

If the body is expected to be empty, the bodyElementDescription field of the 
                <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_description">WS_MESSAGE_DESCRIPTION</a> may be <b>NULL</b>.
            

If the bodyElementDescription is non-<b>NULL</b>, then this function deserializes the 
                body as described in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbody">WsReadBody</a>.
            

After a message has been received, its headers can be inspected using <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheader">WsGetHeader</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsgetcustomheader">WsGetCustomHeader</a>.