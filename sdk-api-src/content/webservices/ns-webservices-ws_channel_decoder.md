---
UID: NS:webservices._WS_CHANNEL_DECODER
title: WS_CHANNEL_DECODER (webservices.h)
description: A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a received message.
helpviewer_keywords: ["WS_CHANNEL_DECODER","WS_CHANNEL_DECODER structure [Web Services for Windows]","webservices/WS_CHANNEL_DECODER","wsw.ws_channel_decoder"]
old-location: wsw\ws_channel_decoder.htm
tech.root: wsw
ms.assetid: d634f203-cf98-4f4e-85ce-5df23653a3ad
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_DECODER, WS_CHANNEL_DECODER structure [Web Services for Windows], webservices/WS_CHANNEL_DECODER, wsw.ws_channel_decoder
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
req.typenames: WS_CHANNEL_DECODER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CHANNEL_DECODER
 - webservices/_WS_CHANNEL_DECODER
 - WS_CHANNEL_DECODER
 - webservices/WS_CHANNEL_DECODER
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
 - WS_CHANNEL_DECODER
---

# WS_CHANNEL_DECODER structure


## -description

A structure that is used to specify a set of callbacks
                that can transform the content type and encoded bytes of a received message.

## -struct-fields

### -field createContext

A context that will be passed to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_decoder_callback">WS_CREATE_DECODER_CALLBACK</a>.

### -field createDecoderCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_decoder_callback">WS_CREATE_DECODER_CALLBACK</a> callback that creates an instance of a decoder.

### -field decoderGetContentTypeCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_get_content_type_callback">WS_DECODER_GET_CONTENT_TYPE_CALLBACK</a> callback that is invoked to get the content type of the message.

### -field decoderStartCallback

A 
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_start_callback">WS_DECODER_START_CALLBACK</a> callback that is invoked at the start of decoding a message.

### -field decoderDecodeCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_decode_callback">WS_DECODER_DECODE_CALLBACK</a> callback that is invoked to decode a message.

### -field decoderEndCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_end_callback">WS_DECODER_END_CALLBACK</a> callback that is invoked at the end of decoding a message.

### -field freeDecoderCallback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_decoder_callback">WS_FREE_DECODER_CALLBACK</a> callback that frees an instance of a decoder.

## -remarks

A <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> may wish to decompress, modify, or otherwise transform
                the encoded bytes of a message as soon as they are received. A <b>WS_CHANNEL_DECODER</b> 
                provides the necessary hooks to intercept and perform these modifications.
            

When creating the channel, the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_DECODER</a> should be
                set with the appropriate functions.
            

The callbacks specified will get invoked according to the following grammar:
              


              


``` syntax

decodercalls := create decoderloop* free
decoderloop  := decodestart
             |  decodestart getcontenttype
             |  decodestart getcontenttype (decode*)
             |  decodestart getcontenttype (decode*) decodeend
```

The decoder may not see the full decode sequence for a message if the channel 
              or the decoder encounters an error while reading the message.  A decoder must be 
              prepared to handle transitioning to the appropriate state based upon the callbacks invoked.
            

When using <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_TCP_CHANNEL_BINDING</a> with <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE_SESSION</a>, the content type
              is fixed for the channel.  In this case, the <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_get_content_type_callback">WS_DECODER_GET_CONTENT_TYPE_CALLBACK</a> must return
              exactly the same value for the content type of every message.
            

The <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_end_callback">WS_DECODER_END_CALLBACK</a> will not be invoked until <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_decode_callback">WS_DECODER_DECODE_CALLBACK</a> returns 0 bytes.
            

When the channel is finished using the decoder instance it will free it via the 
                <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_decoder_callback">WS_FREE_DECODER_CALLBACK</a>.
