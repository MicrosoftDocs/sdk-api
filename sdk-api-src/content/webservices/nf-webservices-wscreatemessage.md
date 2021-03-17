---
UID: NF:webservices.WsCreateMessage
title: WsCreateMessage function (webservices.h)
description: Creates a message object with the specified properties.
helpviewer_keywords: ["WsCreateMessage","WsCreateMessage function [Web Services for Windows]","webservices/WsCreateMessage","wsw.wscreatemessage"]
old-location: wsw\wscreatemessage.htm
tech.root: wsw
ms.assetid: 1c48647e-9e77-4b7a-add3-e035c7f9f27e
ms.date: 12/05/2018
ms.keywords: WsCreateMessage, WsCreateMessage function [Web Services for Windows], webservices/WsCreateMessage, wsw.wscreatemessage
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
 - WsCreateMessage
 - webservices/WsCreateMessage
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
 - WsCreateMessage
---

# WsCreateMessage function


## -description

Creates a <a href="/windows/desktop/wsw/message">message</a> object with the specified properties.

## -parameters

### -param envelopeVersion [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION</a> enumeration value that specifies the version of the envelope for the message.

### -param addressingVersion [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION</a> that specifies the version of the addressing for the message.

### -param properties

An array of optional properties for the message. See <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_property">WS_MESSAGE_PROPERTY</a>.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param message

On   success, a pointer that receives the address of a  <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure representing the new message.
                

When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

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

A message object is the delivery vehicle for Windows Web Services. A single message object can be used to send or  receive sequential messages. Reusing a message object in this way can reduce memory allocations.
            When you no longer need the message, you must free the memory by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a>. (For more information on reusing message objects, see <a href="/windows/desktop/api/webservices/nf-webservices-wsresetmessage">WsResetMessage</a> .)
            

If you are creating a message for use with a particular channel,  use the <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemessageforchannel">WsCreateMessageForChannel</a> function, which will ensure the correct message version for the channel.