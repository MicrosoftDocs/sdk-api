---
UID: NS:webservices._WS_CHANNEL_ENCODER
title: WS_CHANNEL_ENCODER
author: windows-sdk-content
description: A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a sent message.
old-location: wsw\ws_channel_encoder.htm
tech.root: wsw
ms.assetid: 94ff7082-5cc7-46f3-8eec-d38565bbdb23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_CHANNEL_ENCODER, WS_CHANNEL_ENCODER structure [Web Services for Windows], webservices/WS_CHANNEL_ENCODER, wsw.ws_channel_encoder
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_CHANNEL_ENCODER
product: Windows
targetos: Windows
req.typenames: WS_CHANNEL_ENCODER
req.redist: 
---

# WS_CHANNEL_ENCODER structure


## -description


A structure that is used to specify a set of callbacks
                that can transform the content type and encoded bytes of a sent message.
            


## -struct-fields




### -field createContext

A context that will be passed to the <a href="https://msdn.microsoft.com/47a68722-0c99-478a-b1ce-2982287e6a74">WS_CREATE_ENCODER_CALLBACK</a>.
                


### -field createEncoderCallback

A <a href="https://msdn.microsoft.com/47a68722-0c99-478a-b1ce-2982287e6a74">WS_CREATE_ENCODER_CALLBACK</a> callback that creates an instance of an encoder.
                


### -field encoderGetContentTypeCallback

A <a href="https://msdn.microsoft.com/9e17481e-91ed-4215-983e-218936a1aa4f">WS_ENCODER_GET_CONTENT_TYPE_CALLBACK</a> callback that is invoked when a message is to be encoded.
                


### -field encoderStartCallback

A <a href="https://msdn.microsoft.com/308e3d24-e3df-4dc8-a727-d3d8ebe8d5d4">WS_ENCODER_START_CALLBACK</a> callback that is invoked to start encoding a message.
                


### -field encoderEncodeCallback

A 
                    <a href="https://msdn.microsoft.com/f3b191b2-a92f-491d-bd77-500e2d3b37e8">WS_ENCODER_ENCODE_CALLBACK</a> callback that is invoked to encode a message.
                


### -field encoderEndCallback

A <a href="https://msdn.microsoft.com/ab0f88f7-e2b4-48e0-9041-ac4aa66f1575">WS_ENCODER_END_CALLBACK</a> callback that is invoked to at the end of encoding a message.
                


### -field freeEncoderCallback

A <a href="https://msdn.microsoft.com/4ef8fc85-fe98-4c1c-9f8f-77fd4ad3283f">WS_FREE_ENCODER_CALLBACK</a> callback that frees an instance of an encoder.
                


## -remarks



A <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> may wish to compress, modify, or otherwise transform
                the encoded bytes of a message before they are sent. A <b>WS_CHANNEL_ENCODER</b> 
                provides the necessary hooks to intercept and perform these modifications.
            

When creating the channel, the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ENCODER</a> should be
                set with the appropriate functions.
            

The grammar for the encoder callbacks is:

<pre class="syntax" xml:space="preserve"><code>
encodercalls := create encoderloop* free
encoderloop  := getcontenttype
             |  getcontenttype encodestart
             |  getcontenttype encodestart (encode*)
             |  getcontenttype encodestart (encode*) encodeend
</code></pre>
The encoder may not see the full encode sequence for a message if the channel or the 
              encoder encounters an error while writing the message.  An encoder must be prepared to 
              handle transitioning to the appropriate state based upon the callbacks invoked.


When using <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_SESSION</a>, the content type
              is fixed for the channel.  In this case, the <a href="https://msdn.microsoft.com/9e17481e-91ed-4215-983e-218936a1aa4f">WS_ENCODER_GET_CONTENT_TYPE_CALLBACK</a> must return
              exactly the same value for the content type of every message.
            

When the channel is finished using the encoder instance it will free it via the
                <a href="https://msdn.microsoft.com/4ef8fc85-fe98-4c1c-9f8f-77fd4ad3283f">WS_FREE_ENCODER_CALLBACK</a>.
            



