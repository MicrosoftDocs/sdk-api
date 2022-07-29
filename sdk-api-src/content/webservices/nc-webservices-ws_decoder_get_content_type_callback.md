---
UID: NC:webservices.WS_DECODER_GET_CONTENT_TYPE_CALLBACK
title: WS_DECODER_GET_CONTENT_TYPE_CALLBACK (webservices.h)
description: Gets the content type of the message. (WS_DECODER_GET_CONTENT_TYPE_CALLBACK)
helpviewer_keywords: ["WS_DECODER_GET_CONTENT_TYPE_CALLBACK","WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback","WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback function [Web Services for Windows]","webservices/WS_DECODER_GET_CONTENT_TYPE_CALLBACK","wsw.ws_decoder_get_content_type_callback"]
old-location: wsw\ws_decoder_get_content_type_callback.htm
tech.root: wsw
ms.assetid: 8920259f-e52d-4141-87ff-0e1ac1396517
ms.date: 12/05/2018
ms.keywords: WS_DECODER_GET_CONTENT_TYPE_CALLBACK, WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback, WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback function [Web Services for Windows], webservices/WS_DECODER_GET_CONTENT_TYPE_CALLBACK, wsw.ws_decoder_get_content_type_callback
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
 - WS_DECODER_GET_CONTENT_TYPE_CALLBACK
 - webservices/WS_DECODER_GET_CONTENT_TYPE_CALLBACK
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
 - WS_DECODER_GET_CONTENT_TYPE_CALLBACK
---

# WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback function


## -description

Gets the content type of the message.

## -parameters

### -param decoderContext [in]

The encoder instance returned by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_decoder_callback">WS_CREATE_DECODER_CALLBACK</a>.

### -param contentType [in]

The content type of the encoded message.

### -param contentEncoding [in, optional]

The content encoding for the encoded message.

### -param newContentType [out]

The callback should return the content type for the newly decoded message here.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

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

The callback should verify that the content type provided matches what is expected,
              and then should return the content type of the decoded message.
            

The content type returned must remain valid until the next time the callback is
              invoked, or the decoder is freed.
            

The callback has to set newContentType to one that is supported by underlying channel.
                For example, with TCP session channel using SOAP 1.2 and binary encoding, 
                the new content type should always be application/soap+msbinsession1.
            

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> the content encoding parameter will
              be set to the value of the "Content-Encoding" HTTP header.  If this header does
              not exist, then <b>NULL</b> will be passed.
            

For all other channel bindings, <b>NULL</b> will be passed for the content encoding.
