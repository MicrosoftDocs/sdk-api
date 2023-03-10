---
UID: NC:webservices.WS_MESSAGE_DONE_CALLBACK
title: WS_MESSAGE_DONE_CALLBACK (webservices.h)
description: Notifies the caller that the message has completed its use of either the WS_XML_READER structure that was supplied to WsReadEnvelopeStartfunction, or of the WS_XML_WRITER structure supplied to the WsWriteEnvelopeStart function.
helpviewer_keywords: ["WS_MESSAGE_DONE_CALLBACK","WS_MESSAGE_DONE_CALLBACK callback","WS_MESSAGE_DONE_CALLBACK callback function [Web Services for Windows]","webservices/WS_MESSAGE_DONE_CALLBACK","wsw.ws_message_done_callback"]
old-location: wsw\ws_message_done_callback.htm
tech.root: wsw
ms.assetid: 59ab7cbe-dc66-4e74-bec9-ffb25173ff87
ms.date: 12/05/2018
ms.keywords: WS_MESSAGE_DONE_CALLBACK, WS_MESSAGE_DONE_CALLBACK callback, WS_MESSAGE_DONE_CALLBACK callback function [Web Services for Windows], webservices/WS_MESSAGE_DONE_CALLBACK, wsw.ws_message_done_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_MESSAGE_DONE_CALLBACK
 - webservices/WS_MESSAGE_DONE_CALLBACK
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
 - WS_MESSAGE_DONE_CALLBACK
---

# WS_MESSAGE_DONE_CALLBACK callback function


## -description

Notifies the caller that the message has completed its use of either the <a href="/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> structure that was supplied to <a href="/windows/desktop/api/webservices/nf-webservices-wsreadenvelopestart">WsReadEnvelopeStart</a> function, or of the <a href="/windows/desktop/wsw/ws-xml-writer">WS_XML_WRITER</a> structure supplied to the  <a href="/windows/desktop/api/webservices/nf-webservices-wswriteenvelopestart">WsWriteEnvelopeStart</a> function.

## -parameters

### -param doneCallbackState [in]

A pointer to <b>state</b> information passed to the  <a href="/windows/desktop/api/webservices/nf-webservices-wsreadenvelopestart">WsReadEnvelopeStart</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wswriteenvelopestart">WsWriteEnvelopeStart</a> function.
                

This parameter can be used to specify a pointer to user-defined
                    data required by the callback.

## -remarks

This callback can be used as an indicator that the message object is no
                longer using the reader or writer.
            

The callback is specified when <a href="/windows/desktop/api/webservices/nf-webservices-wsreadenvelopestart">WsReadEnvelopeStart</a> or
                <a href="/windows/desktop/api/webservices/nf-webservices-wswriteenvelopestart">WsWriteEnvelopeStart</a> is called.
            

The callback should assume that it is invoked as a 
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_callback_model">WS_SHORT_CALLBACK</a>, since it will be invoked on the same 
                thread that calls <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemessage">WsFreeMessage</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsresetmessage">WsResetMessage</a>.
