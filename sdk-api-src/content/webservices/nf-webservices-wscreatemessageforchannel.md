---
UID: NF:webservices.WsCreateMessageForChannel
title: WsCreateMessageForChannel function (webservices.h)
description: Creates a message for use with a specified channel.
helpviewer_keywords: ["WsCreateMessageForChannel","WsCreateMessageForChannel function [Web Services for Windows]","webservices/WsCreateMessageForChannel","wsw.wscreatemessageforchannel"]
old-location: wsw\wscreatemessageforchannel.htm
tech.root: wsw
ms.assetid: 0a4f076b-6725-45a9-8817-5dec3b647c4f
ms.date: 12/05/2018
ms.keywords: WsCreateMessageForChannel, WsCreateMessageForChannel function [Web Services for Windows], webservices/WsCreateMessageForChannel, wsw.wscreatemessageforchannel
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
 - WsCreateMessageForChannel
 - webservices/WsCreateMessageForChannel
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
 - WsCreateMessageForChannel
---

# WsCreateMessageForChannel function


## -description

Creates a <a href="/windows/desktop/wsw/message">message</a> for use with a specified <a href="/windows/desktop/wsw/channel">channel</a>.

## -parameters

### -param channel [in]

Pointer to a <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> structure representing the channel for the message.

### -param properties

An array of optional properties for the message. See <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_property">WS_MESSAGE_PROPERTY</a>.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param message

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure representing the new message.
                

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

In contrast to the more general  <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemessage">WsCreateMessage</a> function,  <b>WsCreateMessageForChannel</b> ensures that
                the message version used is appropriate for the channel.