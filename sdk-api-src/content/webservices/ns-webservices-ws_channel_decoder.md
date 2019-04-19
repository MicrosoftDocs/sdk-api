---
UID: NS:webservices._WS_CHANNEL_DECODER
title: WS_CHANNEL_DECODER (webservices.h)
author: windows-sdk-content
description: A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a received message.
old-location: wsw\ws_channel_decoder.htm
tech.root: wsw
ms.assetid: d634f203-cf98-4f4e-85ce-5df23653a3ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_DECODER, WS_CHANNEL_DECODER structure [Web Services for Windows], webservices/WS_CHANNEL_DECODER, wsw.ws_channel_decoder
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CHANNEL_DECODER
product: Windows
targetos: Windows
req.typenames: WS_CHANNEL_DECODER
req.redist: 
ms.custom: 19H1
---

# WS_CHANNEL_DECODER structure


## -description


A structure that is used to specify a set of callbacks
                that can transform the content type and encoded bytes of a received message.
            


## -struct-fields




### -field createContext

A context that will be passed to the <a href="https://msdn.microsoft.com/85311349-5c82-4545-8a2b-d8b9e629f04d">WS_CREATE_DECODER_CALLBACK</a>.
                


### -field createDecoderCallback

A <a href="https://msdn.microsoft.com/85311349-5c82-4545-8a2b-d8b9e629f04d">WS_CREATE_DECODER_CALLBACK</a> callback that creates an instance of an decoder.
                


### -field decoderGetContentTypeCallback

A <a href="https://msdn.microsoft.com/8920259f-e52d-4141-87ff-0e1ac1396517">WS_DECODER_GET_CONTENT_TYPE_CALLBACK</a> callback that is invoked to get the content type of the message.
                


### -field decoderStartCallback

A 
                    <a href="https://msdn.microsoft.com/e607b5a2-4d4a-4e23-854d-b5168556bb69">WS_DECODER_START_CALLBACK</a> callback that is invoked at the start of decoding a message.
                


### -field decoderDecodeCallback

A <a href="https://msdn.microsoft.com/04ba9b13-8145-4956-85b2-2330c792665a">WS_DECODER_DECODE_CALLBACK</a> callback that is invoked to decode a message.
                


### -field decoderEndCallback

A <a href="https://msdn.microsoft.com/7cf93467-84f6-4ffb-8329-bc1df119087a">WS_DECODER_END_CALLBACK</a> callback that is invoked at the end of decoding a message.
                


### -field freeDecoderCallback

A <a href="https://msdn.microsoft.com/95c8ed10-7077-488e-affd-1a13b44decb6">WS_FREE_DECODER_CALLBACK</a> callback that frees an instance of an decoder.
                


## -remarks



A <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> may wish to decompress, modify, or otherwise transform
                the encoded bytes of a message as soon as they are received. A <b>WS_CHANNEL_DECODER</b> 
                provides the necessary hooks to intercept and perform these modifications.
            

When creating the channel, the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_DECODER</a> should be
                set with the appropriate functions.
            

The callbacks specified will get invoked according to the following grammar:
              


              

<pre class="syntax" xml:space="preserve"><code>
decodercalls := create decoderloop* free
decoderloop  := decodestart
             |  decodestart getcontenttype
             |  decodestart getcontenttype (decode*)
             |  decodestart getcontenttype (decode*) decodeend</code></pre>
The decoder may not see the full decode sequence for a message if the channel 
              or the decoder encounters an error while reading the message.  A decoder must be 
              prepared to handle transitioning to the appropriate state based upon the callbacks invoked.
            

When using <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_SESSION</a>, the content type
              is fixed for the channel.  In this case, the <a href="https://msdn.microsoft.com/8920259f-e52d-4141-87ff-0e1ac1396517">WS_DECODER_GET_CONTENT_TYPE_CALLBACK</a> must return
              exactly the same value for the content type of every message.
            

The <a href="https://msdn.microsoft.com/7cf93467-84f6-4ffb-8329-bc1df119087a">WS_DECODER_END_CALLBACK</a> will not be invoked until <a href="https://msdn.microsoft.com/04ba9b13-8145-4956-85b2-2330c792665a">WS_DECODER_DECODE_CALLBACK</a> returns 0 bytes.
            

When the channel is finished using the decoder instance it will free it via the 
                <a href="https://msdn.microsoft.com/95c8ed10-7077-488e-affd-1a13b44decb6">WS_FREE_DECODER_CALLBACK</a>.
            



