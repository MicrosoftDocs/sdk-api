---
UID: NF:webservices.WsInitializeMessage
title: WsInitializeMessage function (webservices.h)
description: This function initializes the headers for the message in preparation for processing.
helpviewer_keywords: ["WsInitializeMessage","WsInitializeMessage function [Web Services for Windows]","webservices/WsInitializeMessage","wsw.wsinitializemessage"]
old-location: wsw\wsinitializemessage.htm
tech.root: wsw
ms.assetid: 26eafc5f-6636-4f96-a037-7935cdac5900
ms.date: 12/05/2018
ms.keywords: WsInitializeMessage, WsInitializeMessage function [Web Services for Windows], webservices/WsInitializeMessage, wsw.wsinitializemessage
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
 - WsInitializeMessage
 - webservices/WsInitializeMessage
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
 - WsInitializeMessage
---

# WsInitializeMessage function


## -description

This function initializes the headers for the message in preparation for
                processing.
            After a message has been initialized an application can
                add additional headers.
            On success the message is in <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_INITIALIZED</a> state.
                If the function fails, then no state transitions occurs.

## -parameters

### -param message [in]

A pointer to the Message object to initialize.  The Message must be a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object instance returned
                    by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemessage">WsCreateMessage</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemessageforchannel">WsCreateMessageForChannel</a> and may not be NULL.

### -param initialization [in]

Defines the Message initialization. 
                

<div class="alert"><b>Note</b>  If the  <i>initialization</i> value is set to <b>WS_REPLY_MESSAGE</b> or
                <b>WS_FAULT_MESSAGE</b> the message is automatically addressed.
            </div>
<div> </div>

### -param sourceMessage [in, optional]

A pointer to a message object that is used to initialize the <i>message</i> parameter.
                    This value should be NULL unless the initialization parameter
                    has the value of <b>WS_DUPLICATE_MESSAGE</b>,
                    <b>WS_REPLY_MESSAGE</b>, or <b>WS_FAULT_MESSAGE</b>.

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

The initial sender of a message should add an action header
                to the message using <a href="/windows/desktop/api/webservices/nf-webservices-wssetheader">WsSetHeader</a>.
            

This API must be called before <a href="/windows/desktop/api/webservices/nf-webservices-wswriteenvelopestart">WsWriteEnvelopeStart</a> or
                <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a> is called for the message.