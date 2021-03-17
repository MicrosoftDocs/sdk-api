---
UID: NC:webservices.WS_READ_MESSAGE_START_CALLBACK
title: WS_READ_MESSAGE_START_CALLBACK (webservices.h)
description: Handles the WsReadMessageStart call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_READ_MESSAGE_START_CALLBACK","WS_READ_MESSAGE_START_CALLBACK callback","WS_READ_MESSAGE_START_CALLBACK callback function [Web Services for Windows]","webservices/WS_READ_MESSAGE_START_CALLBACK","wsw.ws_read_message_start_callback"]
old-location: wsw\ws_read_message_start_callback.htm
tech.root: wsw
ms.assetid: e9c5d9df-2f96-472d-ba9d-ecb7ccac4a13
ms.date: 12/05/2018
ms.keywords: WS_READ_MESSAGE_START_CALLBACK, WS_READ_MESSAGE_START_CALLBACK callback, WS_READ_MESSAGE_START_CALLBACK callback function [Web Services for Windows], webservices/WS_READ_MESSAGE_START_CALLBACK, wsw.ws_read_message_start_callback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_READ_MESSAGE_START_CALLBACK
 - webservices/WS_READ_MESSAGE_START_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_READ_MESSAGE_START_CALLBACK
---

# WS_READ_MESSAGE_START_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param message [in]

The message to receive into.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.

### -param error [in, optional]

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Start of message was received successfully.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_S_END</b></dt>
</dl>
</td>
<td width="60%">
There are no more messages available on the channel.
                

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

See <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> for information about the contract
                of this API.
