---
UID: NF:webservices.WsGetMappedHeader
title: WsGetMappedHeader function (webservices.h)
description: Finds a mapped header in the message and deserializes it.
helpviewer_keywords: ["WsGetMappedHeader","WsGetMappedHeader function [Web Services for Windows]","webservices/WsGetMappedHeader","wsw.wsgetmappedheader"]
old-location: wsw\wsgetmappedheader.htm
tech.root: wsw
ms.assetid: abdff5ca-fb0d-4867-b729-5cfe18520f80
ms.date: 12/05/2018
ms.keywords: WsGetMappedHeader, WsGetMappedHeader function [Web Services for Windows], webservices/WsGetMappedHeader, wsw.wsgetmappedheader
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsGetMappedHeader
 - webservices/WsGetMappedHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetMappedHeader
---

# WsGetMappedHeader function


## -description

Finds a mapped header in the message and deserializes it.

## -parameters

### -param message [in]

The message containing the header.
                

The message can be in any state but <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

### -param headerName [in]

The name of the mapped header.

### -param repeatingOption [in]

Whether the header may appear more than once in
                    the message.
                

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_repeating_header_option">WS_REPEATING_HEADER</a> is used, then
                    the header index indicates which of the headers
                    with the specified headerName to return.
                

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_repeating_header_option">WS_SINGLETON_HEADER</a> is used, then
                    the headerIndex must be zero.

### -param headerIndex [in]

The zero-based index of the header within
                    the set of headers with the specified headerName.

### -param valueType [in]

The type of value to deserialize.

### -param readOption [in]

Whether the value is required, and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.
                

If the header is optional (may appear zero or one times), then
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTIONAL_POINTER</a> can be used.

### -param heap [in, optional]

The heap to store the deserialized header data in.
                    If this is <b>NULL</b>, then the message heap will be used.

### -param value

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The header does not exist, and is required.
                

The input data was not in the expected format.
                


<a href="/windows/desktop/api/webservices/ne-webservices-ws_repeating_header_option">WS_SINGLETON_HEADER</a> was specified, and there are
                    multiple instances of the header with the specified name in the message.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The size quota of the heap was exceeded.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to deserialize the header.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are incorrect.
                

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

A message may contain additional transport-specific information that is
                not part of the message envelope.  This transport-specific information
                can be exposed programmatically as headers of the Message object.
                This function is used to read a header that has been mapped by a
                transport into the message.
            

When using the HTTP channel, the required mappings must be specified before headers
                can be extracted with this function.  For more information, see <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_message_mapping">WS_HTTP_MESSAGE_MAPPING</a>.