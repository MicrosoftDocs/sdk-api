---
UID: NF:webservices.WsSendReplyMessage
title: WsSendReplyMessage function (webservices.h)
author: windows-sdk-content
description: Sends a message which is a reply to a received message.
old-location: wsw\wssendreplymessage.htm
tech.root: wsw
ms.assetid: cabfd07b-294c-4e3a-9d50-84d9b4d98f62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsSendReplyMessage, WsSendReplyMessage function [Web Services for Windows], webservices/WsSendReplyMessage, wsw.wssendreplymessage
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
 - WsSendReplyMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsSendReplyMessage function


## -description


Sends a message which is a reply to a received message.
            


## -parameters




### -param channel [in]

A pointer to the <b>Channel</b> object on which to send the reply Message.  The pointer must reference a valid <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> object.
                
                


### -param replyMessage [in]

A pointer to the <b>Message</b> object for sending the reply.  The pointer must reference a valid <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> object.
                
                Message object state must be set to <b>WS_MESSAGE_STATE_EMPTY</b>  or
                  <b>WS_MESSAGE_STATE_INITIALIZED</b>.
                <div class="alert"><b>Note</b>  If an initialized message is provided
                  it must be initialized using <b>WS_REPLY_MESSAGE</b> or 
                  <b>WS_FAULT_MESSAGE</b>.
                </div>
<div> </div>



### -param replyMessageDescription [in]

A pointer to a <a href="https://msdn.microsoft.com/399b3363-004b-499a-9726-0b2513826f43">WS_MESSAGE_DESCRIPTION</a> object.  The <b>action</b> field of <b>WS_MESSAGE_DESCRIPTION</b> is used as the
                    <b>action</b> header for the reply message.  This field can be <b>NULL</b> if no action
                    is required.
                

The <b>bodyElementDescription</b>  field of the <a href="https://msdn.microsoft.com/399b3363-004b-499a-9726-0b2513826f43">WS_MESSAGE_DESCRIPTION</a>is used to serialize the body of the reply message.  This field may be 
                    <b>NULL</b> if no body element is desired.  See <a href="https://msdn.microsoft.com/70ff43f5-6f1a-4bbb-aa39-6fb9476e6a37">WsWriteBody</a> for information
                    about how the <b>bodyElementDescription</b> is used to serialize a value.
                


### -param writeOption [in]

Determines whether the body element is required, and how the value is allocated.
                    See <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> for more information.
                


### -param replyBodyValue

A void pointer to the value to serialize in the reply message.
                


### -param replyBodyValueSize [in]

The size  in bytes of the reply value being serialized.
                


### -param requestMessage [in]

A pointer to a WS_MESSAGE object encapsulating the request message text.  This is used to obtain correlation information used
                    in formulating the reply message.
                <div class="alert"><b>Note</b>  The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b>.
                </div>
<div> </div>





### -param asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> data structure with information about invoking the function asynchronously.  A <b>NULL</b> 
                 value indicates a request for synchronous operation.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
                to the <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION</a>.  See <a href="https://msdn.microsoft.com/d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19">Channel Layer Overview</a> 
                for more information about correlating request reply messages.
            



