---
UID: NC:webservices.WS_ENCODER_END_CALLBACK
title: WS_ENCODER_END_CALLBACK (webservices.h)
description: Encodes the end of a message.
helpviewer_keywords: ["WS_ENCODER_END_CALLBACK","WS_ENCODER_END_CALLBACK callback","WS_ENCODER_END_CALLBACK callback function [Web Services for Windows]","webservices/WS_ENCODER_END_CALLBACK","wsw.ws_encoder_end_callback"]
old-location: wsw\ws_encoder_end_callback.htm
tech.root: wsw
ms.assetid: ab0f88f7-e2b4-48e0-9041-ac4aa66f1575
ms.date: 12/05/2018
ms.keywords: WS_ENCODER_END_CALLBACK, WS_ENCODER_END_CALLBACK callback, WS_ENCODER_END_CALLBACK callback function [Web Services for Windows], webservices/WS_ENCODER_END_CALLBACK, wsw.ws_encoder_end_callback
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
 - WS_ENCODER_END_CALLBACK
 - webservices/WS_ENCODER_END_CALLBACK
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
 - WS_ENCODER_END_CALLBACK
---

# WS_ENCODER_END_CALLBACK callback function


## -description

Encodes the end of a message.

## -parameters

### -param *encoderContext [in]

The encoder instance returned by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_encoder_callback">WS_CREATE_ENCODER_CALLBACK</a>.

### -param *asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if the function is invoked  synchronously.

### -param *error [in, optional]

Where additional error information should be stored if the function fails.

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

The encoder can use the callback passed to <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_encoder_callback">WS_CREATE_ENCODER_CALLBACK</a> to
            write the encoded data of the message.