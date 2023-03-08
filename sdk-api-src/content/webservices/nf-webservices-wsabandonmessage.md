---
UID: NF:webservices.WsAbandonMessage
title: WsAbandonMessage function (webservices.h)
description: Skips the remainder of a specified message on a specified channel.
helpviewer_keywords: ["WsAbandonMessage","WsAbandonMessage function [Web Services for Windows]","webservices/WsAbandonMessage","wsw.wsabandonmessage"]
old-location: wsw\wsabandonmessage.htm
tech.root: wsw
ms.assetid: b8f5da50-d296-4550-8810-114d1f0e810b
ms.date: 12/05/2018
ms.keywords: WsAbandonMessage, WsAbandonMessage function [Web Services for Windows], webservices/WsAbandonMessage, wsw.wsabandonmessage
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
 - WsAbandonMessage
 - webservices/WsAbandonMessage
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
 - WsAbandonMessage
---

# WsAbandonMessage function


## -description

Skips the remainder of a specified <a href="/windows/desktop/wsw/message">message</a> on a specified channel.

## -parameters

### -param channel [in]

Pointer to a <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> structure representing the channel on which the message is being read or written.

### -param message [in]

Pointer to a <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure representing the message to abandon.  This should be
                    the same message that was passed to the <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a> 
                    or <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> function.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure that receives additional error information if the function fails.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The channel is not in the WS_CHANNEL_STATE_OPEN or  WS_CHANNEL_STATE_FAULTED state.
                (For channel states, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE</a> enumeration.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified message is not currently being read or written on the specified channel.
                

</td>
</tr>
</table>

## -remarks

<b>WsAbandonMessage</b> is used to skip reading or writing the remaining contents of a message, 
                allowing the next message for the channel to be read or written.  In this respect, it is an alternative to 
                the <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessageend">WsReadMessageEnd</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessageend">WsWriteMessageEnd</a> functions, as shown in the following
                state diagram:
            
:::image type="content" source="./images/AbandonMessage.png" border="false" alt-text="Diagram showing how the state transitions caused by the WsAbandonMessage function differ from the WSReadMessageEnd and WsWriteMessageEnd functions.":::

For read operations, an application typically calls <b>WsAbandonMessage</b> when it is unnecessary for the application to continue reading the 
                message data, for example, if the
                message does not meet the application's requirements.  This function can also be used 
                if the message contains malformed XML or if the <a href="/windows/desktop/wsw/xml-reader">XML reader</a> has 
                generated an error while reading the message.  

If the channel is streamed 
                (see the WS_STREAMED_INPUT_TRANSFER_MODE value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_TRANSFER_MODE</a> enumeration),  the remainder of the 
                streamed message data is read and automatically discarded with the next call to 
                <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsclosechannel">WsCloseChannel</a> for the 
                channel.  If the channel is not streamed, the unread buffered message data 
                is simply discarded.
            

For write operations, an application typically calls <b>WsAbandonMessage</b> when the application cannot continue writing the message because it has encountered some error, such as one returned by the <a href="/windows/desktop/wsw/xml-writer">XML writer</a>, or must stop generating the message for some other reason.  

If the 
                channel is streamed (see the WS_STREAMED_INPUT_TRANSFER_MODE value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_TRANSFER_MODE</a> enumeration), the message data will be truncated and may result in errors when read by the 
                remote party.  If the channel is not streamed,  the buffered data for the 
                message is simply  discarded (since it was never transmitted).
            

This function allows the user of the channel to keep the channel open and 
                send or receive additional messages (such as sending a fault), even though 
                an error occurred.  In contrast, <a href="/windows/desktop/api/webservices/nf-webservices-wsabortchannel">WsAbortChannel</a> will causes 
                the channel to fault.  A typical usage is first to try to abandon the message and
                send a fault.  If that fails,  the channel can be aborted.
            

This function does not perform any blocking I/O.
            

This function is only valid when the channel is in the WS_CHANNEL_STATE_OPEN 
                 or WS_CHANNEL_STATE_FAULTED states.
            (For channel states, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE</a> enumeration.)

The message specified must be the current message being read or the current message being written
                for the specified channel.
            

If called correctly, this function will not fail (for example, due to lack of system resources).