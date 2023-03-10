---
UID: NC:webservices.WS_DECODER_END_CALLBACK
title: WS_DECODER_END_CALLBACK (webservices.h)
description: Decodes the end of a message.
helpviewer_keywords: ["WS_DECODER_END_CALLBACK","WS_DECODER_END_CALLBACK callback","WS_DECODER_END_CALLBACK callback function [Web Services for Windows]","webservices/WS_DECODER_END_CALLBACK","wsw.ws_decoder_end_callback"]
old-location: wsw\ws_decoder_end_callback.htm
tech.root: wsw
ms.assetid: 7cf93467-84f6-4ffb-8329-bc1df119087a
ms.date: 12/05/2018
ms.keywords: WS_DECODER_END_CALLBACK, WS_DECODER_END_CALLBACK callback, WS_DECODER_END_CALLBACK callback function [Web Services for Windows], webservices/WS_DECODER_END_CALLBACK, wsw.ws_decoder_end_callback
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
 - WS_DECODER_END_CALLBACK
 - webservices/WS_DECODER_END_CALLBACK
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
 - WS_DECODER_END_CALLBACK
---

# WS_DECODER_END_CALLBACK callback function


## -description

Decodes the end of a message.

## -parameters

### -param encoderContext [in]

The decoder instance returned by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_decoder_callback">WS_CREATE_DECODER_CALLBACK</a>.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.

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

The decoder can use the callback passed to <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_decoder_callback">WS_CREATE_DECODER_CALLBACK</a> to
            read the encoded data of the message.
          

This callback is not invoked until <a href="/windows/desktop/api/webservices/nc-webservices-ws_decoder_decode_callback">WS_DECODER_DECODE_CALLBACK</a> returns 0 bytes.
