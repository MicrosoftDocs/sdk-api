---
UID: NC:webservices.WS_CREATE_ENCODER_CALLBACK
title: WS_CREATE_ENCODER_CALLBACK (webservices.h)
description: Handles creating an encoder instance.
helpviewer_keywords: ["WS_CREATE_ENCODER_CALLBACK","WS_CREATE_ENCODER_CALLBACK callback","WS_CREATE_ENCODER_CALLBACK callback function [Web Services for Windows]","webservices/WS_CREATE_ENCODER_CALLBACK","wsw.ws_create_encoder_callback"]
old-location: wsw\ws_create_encoder_callback.htm
tech.root: wsw
ms.assetid: 47a68722-0c99-478a-b1ce-2982287e6a74
ms.date: 12/05/2018
ms.keywords: WS_CREATE_ENCODER_CALLBACK, WS_CREATE_ENCODER_CALLBACK callback, WS_CREATE_ENCODER_CALLBACK callback function [Web Services for Windows], webservices/WS_CREATE_ENCODER_CALLBACK, wsw.ws_create_encoder_callback
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
 - WS_CREATE_ENCODER_CALLBACK
 - webservices/WS_CREATE_ENCODER_CALLBACK
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
 - WS_CREATE_ENCODER_CALLBACK
---

# WS_CREATE_ENCODER_CALLBACK callback function


## -description

Handles creating an encoder instance.

## -parameters

### -param createContext [in]

The createContext that was specified in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_encoder">WS_CHANNEL_ENCODER</a> used during channel creation.

### -param writeCallback [in]

The function that should be used to write the message data.  This callback
                  should only be used in response to the <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_start_callback">WS_ENCODER_START_CALLBACK</a>,
                  <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_encode_callback">WS_ENCODER_ENCODE_CALLBACK</a> and <a href="/windows/desktop/api/webservices/nc-webservices-ws_encoder_end_callback">WS_ENCODER_END_CALLBACK</a> callbacks.

### -param writeContext [in]

The write context that should be passed to the provided <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">WS_WRITE_CALLBACK</a>.
                


#### - **encoderContext

Returns the encoder instance.  This value will be
                    passed to all of the encoder callbacks.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

### -param encoderContext

Returns the encoder instance.  This value will be
                    passed to all of the encoder callbacks.

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

The channel will create encoder instances as necessary.  Each encoder
              instance will be called in a single-threaded fashion.  A single encoder
              instance however should not assume that it will see all messages from a
              channel, as the channel may use multiple encoder instances for processing
              messages.
