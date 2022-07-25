---
UID: NF:webservices.WsWriteEnvelopeStart
title: WsWriteEnvelopeStart function (webservices.h)
description: Writes the start of the message including the current set of headers of the message and prepares to write the body elements.
helpviewer_keywords: ["WsWriteEnvelopeStart","WsWriteEnvelopeStart function [Web Services for Windows]","webservices/WsWriteEnvelopeStart","wsw.wswriteenvelopestart"]
old-location: wsw\wswriteenvelopestart.htm
tech.root: wsw
ms.assetid: 213fe780-82f2-4140-92f2-2665317a5cb6
ms.date: 12/05/2018
ms.keywords: WsWriteEnvelopeStart, WsWriteEnvelopeStart function [Web Services for Windows], webservices/WsWriteEnvelopeStart, wsw.wswriteenvelopestart
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
 - WsWriteEnvelopeStart
 - webservices/WsWriteEnvelopeStart
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
 - WsWriteEnvelopeStart
---

# WsWriteEnvelopeStart function


## -description

Writes the start of the message including the current set of headers of the message and prepares to write the body elements.

This function is designed  for writing messages to destinations other than channels.  To write a message to a channel use <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a>.

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object to write.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.

### -param writer [in]

A pointer to the <b>XML Writer</b> object to write the Message.  The Message object uses the Writer in subsequent calls to write the message.  The caller must keep the writer valid until <a href="/windows/desktop/api/webservices/nf-webservices-wsresetmessage">WsResetMessage</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a> is called.
                
The <a href="/windows/desktop/api/webservices/nc-webservices-ws_message_done_callback">WS_MESSAGE_DONE_CALLBACK</a> parameter can be used to determine that the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> is no longer in use.

### -param doneCallback [in, optional]

The callback function invoked when the Message is released or reset. This callback can be used to indicate that the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> object is no longer
 in use by this message. If this function fails the callback is not called. If the function succeeds the callback is invoked one time only.

### -param doneCallbackState [in, optional]

A void pointer to a user-defined state that will be passed to the specified callback. This parameter may be <b>NULL</b>.

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

The start of the message, including the current set of headers that exist in the message, 
                are written to the writer.
            

The message state must be set to <b>WS_MESSAGE_STATE_INITIALIZED</b>.  On success 
                the Message state transitions to  <b>WS_MESSAGE_STATE_WRITING</b>.  
                On failure state transition does not occur.
            

To write an element of the message body use <a href="/windows/desktop/api/webservices/nf-webservices-wswritebody">WsWriteBody</a>.  To write
                directly to the Writer of the Message obtain the Reader with the  <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_ID</a> set to <b>WS_MESSAGE_PROPERTY_BODY_WRITER</b> property.