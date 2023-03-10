---
UID: NC:webservices.WS_CREATE_DECODER_CALLBACK
title: WS_CREATE_DECODER_CALLBACK (webservices.h)
description: Handles creating a decoder instance.
helpviewer_keywords: ["WS_CREATE_DECODER_CALLBACK","WS_CREATE_DECODER_CALLBACK callback","WS_CREATE_DECODER_CALLBACK callback function [Web Services for Windows]","webservices/WS_CREATE_DECODER_CALLBACK","wsw.ws_create_decoder_callback"]
old-location: wsw\ws_create_decoder_callback.htm
tech.root: wsw
ms.assetid: 85311349-5c82-4545-8a2b-d8b9e629f04d
ms.date: 12/05/2018
ms.keywords: WS_CREATE_DECODER_CALLBACK, WS_CREATE_DECODER_CALLBACK callback, WS_CREATE_DECODER_CALLBACK callback function [Web Services for Windows], webservices/WS_CREATE_DECODER_CALLBACK, wsw.ws_create_decoder_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CREATE_DECODER_CALLBACK
 - webservices/WS_CREATE_DECODER_CALLBACK
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
 - WS_CREATE_DECODER_CALLBACK
---

# WS_CREATE_DECODER_CALLBACK callback function


## -description

Handles creating a decoder instance.

## -parameters

### -param createContext [in]

The createContext that was specified in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_decoder">WS_CHANNEL_DECODER</a> used during channel creation.

### -param readCallback [in]

The function that should be used to read the message data.  This callback
                    should only be used in response to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_start_callback">WS_DECODER_START_CALLBACK</a>,
                    <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_decode_callback">WS_DECODER_DECODE_CALLBACK</a> and <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_end_callback">WS_DECODER_END_CALLBACK</a> 
                    callbacks.

### -param readContext [in]

The read context that should be passed to the provided <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_callback">WS_READ_CALLBACK</a>.
                


#### - **decoderContext

Returns the decoder instance.  This value will be
                    passed to all of the decoder callbacks.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

### -param decoderContext

Returns the decoder instance.  This value will be
                    passed to all of the decoder callbacks.

## -returns

This callback function can return one of these values.

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

The channel will create decoder instances as necessary.  Each decoder
               instance will be called in a single-threaded fashion.  A single decoder 
               instance however should not assume that it will see all messages from a
               channel, as the channel may use multiple decoder instances for processing
               messages.
