---
UID: NS:webservices._WS_CHANNEL_ENCODER
title: WS_CHANNEL_ENCODER (webservices.h)
description: A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a sent message.
helpviewer_keywords: ["WS_CHANNEL_ENCODER","WS_CHANNEL_ENCODER structure [Web Services for Windows]","webservices/WS_CHANNEL_ENCODER","wsw.ws_channel_encoder"]
old-location: wsw\ws_channel_encoder.htm
tech.root: wsw
ms.assetid: 94ff7082-5cc7-46f3-8eec-d38565bbdb23
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_ENCODER, WS_CHANNEL_ENCODER structure [Web Services for Windows], webservices/WS_CHANNEL_ENCODER, wsw.ws_channel_encoder
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
req.typenames: WS_CHANNEL_ENCODER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CHANNEL_ENCODER
 - webservices/_WS_CHANNEL_ENCODER
 - WS_CHANNEL_ENCODER
 - webservices/WS_CHANNEL_ENCODER
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
 - WS_CHANNEL_ENCODER
---

# WS_CHANNEL_ENCODER structure


## -description

A structure that is used to specify a set of callbacks
                that can transform the content type and encoded bytes of a sent message.

## -struct-fields

### -field createContext

A context that will be passed to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_encoder_callback">WS_CREATE_ENCODER_CALLBACK</a>.

### -field createEncoderCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_encoder_callback">WS_CREATE_ENCODER_CALLBACK</a> callback that creates an instance of an encoder.

### -field encoderGetContentTypeCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_get_content_type_callback">WS_ENCODER_GET_CONTENT_TYPE_CALLBACK</a> callback that is invoked when a message is to be encoded.

### -field encoderStartCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_start_callback">WS_ENCODER_START_CALLBACK</a> callback that is invoked to start encoding a message.

### -field encoderEncodeCallback

A 
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_encode_callback">WS_ENCODER_ENCODE_CALLBACK</a> callback that is invoked to encode a message.

### -field encoderEndCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_end_callback">WS_ENCODER_END_CALLBACK</a> callback that is invoked to at the end of encoding a message.

### -field freeEncoderCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_encoder_callback">WS_FREE_ENCODER_CALLBACK</a> callback that frees an instance of an encoder.

## -remarks

A <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> may wish to compress, modify, or otherwise transform
                the encoded bytes of a message before they are sent. A <b>WS_CHANNEL_ENCODER</b> 
                provides the necessary hooks to intercept and perform these modifications.
            

When creating the channel, the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ENCODER</a> should be
                set with the appropriate functions.
            

The grammar for the encoder callbacks is:


``` syntax

encodercalls := create encoderloop* free
encoderloop  := getcontenttype
             |  getcontenttype encodestart
             |  getcontenttype encodestart (encode*)
             |  getcontenttype encodestart (encode*) encodeend

```

The encoder may not see the full encode sequence for a message if the channel or the 
              encoder encounters an error while writing the message.  An encoder must be prepared to 
              handle transitioning to the appropriate state based upon the callbacks invoked.


When using <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_TCP_CHANNEL_BINDING</a> with <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE_SESSION</a>, the content type
              is fixed for the channel.  In this case, the <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_get_content_type_callback">WS_ENCODER_GET_CONTENT_TYPE_CALLBACK</a> must return
              exactly the same value for the content type of every message.
            

When the channel is finished using the encoder instance it will free it via the
                <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_encoder_callback">WS_FREE_ENCODER_CALLBACK</a>.
