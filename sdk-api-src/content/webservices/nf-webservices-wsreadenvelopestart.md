---
UID: NF:webservices.WsReadEnvelopeStart
title: WsReadEnvelopeStart function (webservices.h)
description: Reads the headers of the message and prepare to read the body elements.
helpviewer_keywords: ["WsReadEnvelopeStart","WsReadEnvelopeStart function [Web Services for Windows]","webservices/WsReadEnvelopeStart","wsw.wsreadenvelopestart"]
old-location: wsw\wsreadenvelopestart.htm
tech.root: wsw
ms.assetid: f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6
ms.date: 12/05/2018
ms.keywords: WsReadEnvelopeStart, WsReadEnvelopeStart function [Web Services for Windows], webservices/WsReadEnvelopeStart, wsw.wsreadenvelopestart
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
 - WsReadEnvelopeStart
 - webservices/WsReadEnvelopeStart
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
 - WsReadEnvelopeStart
---

# WsReadEnvelopeStart function


## -description

Reads the headers of the message and prepare to read the body elements. 
            The operation reads the start of the next message from the Reader including the headers of
                the message.
            The process allows for reading of messages from other sources than channels.  To read
                a message using a channel, use <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a>.
            <div class="alert"><b>Note</b>  On success the headers is stored in the message and can be retrieved randomly
                using functions such as <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheader">WsGetHeader</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsgetcustomheader">WsGetCustomHeader</a>.</div>
<div> </div>

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object to read.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object.

### -param reader [in]

A pointer to the Reader with the message to read.  The Message object uses the Reader in the current and subsequent
                    calls.  <div class="alert"><b>Note</b>  The function caller must keep the Reader valid until
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsresetmessage">WsResetMessage</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a> is called.  
                    The <a href="/windows/desktop/api/webservices/nc-webservices-ws_message_done_callback">WS_MESSAGE_DONE_CALLBACK</a> parameter can be used a way to know
                    that the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> is no longer in use.
                </div>
<div> </div>

### -param doneCallback [in, optional]

Identifies the callback function to initiate on success of the current operation once the message has
                    been released. <div class="alert"><b>Note</b>  Messages are released using <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsresetmessage">WsResetMessage</a>
</div>
<div> </div>  The callback
                    can be used to discover whether the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> instance  is in use by this message.  If the current operation  fails the callback is not called.

### -param doneCallbackState [in, optional]

A pointer to user-defined state that can be passed
                    to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_message_done_callback">WS_MESSAGE_DONE_CALLBACK</a>.
                    This parameter may be <b>NULL</b> if the callback is not used.

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

The message must be in <b>WS_MESSAGE_STATE_EMPTY</b> state.  On success
                the message state is set to <b>WS_MESSAGE_STATE_READING</b>. 

To read an Element of the message body, use <a href="/windows/desktop/api/webservices/nf-webservices-wsreadbody">WsReadBody</a>.  To read
                directly from the XML Reader get the Reader with 
                the <b>message property Id</b> set to  <b>WS_MESSAGE_PROPERTY_BODY_READER</b>.