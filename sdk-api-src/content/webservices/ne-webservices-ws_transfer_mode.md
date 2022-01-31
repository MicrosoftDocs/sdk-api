---
UID: NE:webservices.__unnamed_enum_20
title: WS_TRANSFER_MODE (webservices.h)
description: Whether messages that are sent or received are streamed or buffered.
helpviewer_keywords: ["WS_BUFFERED_TRANSFER_MODE","WS_STREAMED_INPUT_TRANSFER_MODE","WS_STREAMED_OUTPUT_TRANSFER_MODE","WS_STREAMED_TRANSFER_MODE","WS_TRANSFER_MODE","WS_TRANSFER_MODE enumeration [Web Services for Windows]","webservices/WS_BUFFERED_TRANSFER_MODE","webservices/WS_STREAMED_INPUT_TRANSFER_MODE","webservices/WS_STREAMED_OUTPUT_TRANSFER_MODE","webservices/WS_STREAMED_TRANSFER_MODE","webservices/WS_TRANSFER_MODE","wsw.ws_transfer_mode"]
old-location: wsw\ws_transfer_mode.htm
tech.root: wsw
ms.assetid: 6153bef6-f37f-4bc6-b1c5-5fbedd6bd234
ms.date: 12/05/2018
ms.keywords: WS_BUFFERED_TRANSFER_MODE, WS_STREAMED_INPUT_TRANSFER_MODE, WS_STREAMED_OUTPUT_TRANSFER_MODE, WS_STREAMED_TRANSFER_MODE, WS_TRANSFER_MODE, WS_TRANSFER_MODE enumeration [Web Services for Windows], webservices/WS_BUFFERED_TRANSFER_MODE, webservices/WS_STREAMED_INPUT_TRANSFER_MODE, webservices/WS_STREAMED_OUTPUT_TRANSFER_MODE, webservices/WS_STREAMED_TRANSFER_MODE, webservices/WS_TRANSFER_MODE, wsw.ws_transfer_mode
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
req.typenames: WS_TRANSFER_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_TRANSFER_MODE
 - webservices/WS_TRANSFER_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_TRANSFER_MODE
---

# WS_TRANSFER_MODE enumeration


## -description

Whether messages that are sent or received are streamed or buffered.

## -enum-fields

### -field WS_STREAMED_INPUT_TRANSFER_MODE:0x1

Setting this flag means messages are delivered in chunks.  The start of the message
                    (opening tag, headers, and opening body tag) will be returned to the application
                    when <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> completes.  It is up to the application to call
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsfillbody">WsFillBody</a> before reading each chunk of the message body.  The end of
                    the message (closing body and envelope tags) will be read when <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessageend">WsReadMessageEnd</a> is called.
                

Not setting this flag means the entire message is read and buffered
                    in memory before <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a> indicates completion.

### -field WS_STREAMED_OUTPUT_TRANSFER_MODE:0x2

Setting this flag means messages are transmitted in chunks.  The start of the message (opening
                    envelope tag, headers, and opening body tag) will be transmitted when <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a> is called.  It is up to the application to call <a href="/windows/desktop/api/webservices/nf-webservices-wsflushbody">WsFlushBody</a> after writing each chunk 
                    of the message body to cause the chunk to be transmitted.
                    Any remaining body data will be transmitted when <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessageend">WsWriteMessageEnd</a> is called, along with
                    the end of the message (closing body and envelope tags).
                

Not setting this flag means the entire message is buffered in 
                    memory and is only transmitted once <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessageend">WsWriteMessageEnd</a> is called.

### -field WS_BUFFERED_TRANSFER_MODE:0x0

Messages that are written or read are buffered.
                

This is equivalent to specifying neither
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_STREAMED_INPUT_TRANSFER_MODE</a> nor
                    <b>WS_STREAMED_OUTPUT_TRANSFER_MODE</b>.

### -field WS_STREAMED_TRANSFER_MODE

Messages that are written or read are streamed.
                

This is equivalent to specifying both
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_transfer_mode">WS_STREAMED_INPUT_TRANSFER_MODE</a> and
                    <b>WS_STREAMED_OUTPUT_TRANSFER_MODE</b>.

## -remarks

This value is specified for a channel using the 
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_TRANSFER_MODE</a> channel property.
            

The streaming programming model can be used regardless of which 
                transfer mode is used.  In the case where streaming is not used, the calls
                to the calls to <a href="/windows/desktop/api/webservices/nf-webservices-wsfillbody">WsFillBody</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsflushbody">WsFlushBody</a> are NOPs.
