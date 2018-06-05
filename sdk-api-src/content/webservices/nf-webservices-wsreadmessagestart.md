---
UID: NF:webservices.WsReadMessageStart
title: WsReadMessageStart function
author: windows-sdk-content
description: Read the headers of the next message from the channel, and prepare to read the body elements.
old-location: wsw\wsreadmessagestart.htm
old-project: wsw
ms.assetid: e4f92e99-f272-47b5-8eaa-56713b22df7e
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsReadMessageStart, WsReadMessageStart function [Web Services for Windows], webservices/WsReadMessageStart, wsw.wsreadmessagestart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsReadMessageStart
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadMessageStart function


## -description



                Read the headers of the next message from the channel, and prepare to read the body elements.
            


## -parameters




### -param channel [in]


                    The channel to receive from.
                


### -param message [in]


                    The message to receive into.
                


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




                This reads the start of the next message from the channel, including the headers of
                the message.
            


                This function is like <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a> but is used with channels.
            


                Upon success, the headers will be stored in the message and can be accessed in a random-access
                fashion (for example, using <a href="https://msdn.microsoft.com/ff6e639f-715d-4a4f-b0ef-35202aa54dc5">WsGetHeader</a>).
            


                The message must be in <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a> state.  Upon success,
                the message will have transitioned to <b>WS_MESSAGE_STATE_READING</b> state.
            


                To deserialize an element of the message body, use <a href="https://msdn.microsoft.com/43ceeb1e-aeb2-4482-90f0-d7f6013b239f">WsReadBody</a>.  To read
                directly from the XML Reader of the message, first get the reader using
                the <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_BODY_READER</a> property.
            


                If the channel input is streamed (<a href="https://msdn.microsoft.com/6153bef6-f37f-4bc6-b1c5-5fbedd6bd234">WS_STREAMED_INPUT_TRANSFER_MODE</a>), then
                <a href="https://msdn.microsoft.com/fe70338d-d2bf-4126-96b2-30ef6ebfa74d">WsFillBody</a> must be called to receive the next part of the body before
                it is actually read.
            



