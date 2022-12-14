---
UID: NF:webservices.WsGetCustomHeader
title: WsGetCustomHeader function (webservices.h)
description: Finds an application-defined header of the message and deserializes it.
helpviewer_keywords: ["WsGetCustomHeader","WsGetCustomHeader function [Web Services for Windows]","webservices/WsGetCustomHeader","wsw.wsgetcustomheader"]
old-location: wsw\wsgetcustomheader.htm
tech.root: wsw
ms.assetid: bdfb441b-afc4-4be8-b437-f299a31ce84b
ms.date: 12/05/2018
ms.keywords: WsGetCustomHeader, WsGetCustomHeader function [Web Services for Windows], webservices/WsGetCustomHeader, wsw.wsgetcustomheader
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
 - WsGetCustomHeader
 - webservices/WsGetCustomHeader
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
 - WsGetCustomHeader
---

# WsGetCustomHeader function


## -description

Finds an application-defined header of the message and deserializes it.

## -parameters

### -param message [in]

The message containing the header.
                

The message can be in any state but <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

### -param customHeaderDescription [in]

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_element_description">WS_ELEMENT_DESCRIPTION</a> which describes the header element.

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

### -param readOption [in]

Whether the value is required, and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.

### -param heap [in, optional]

The heap to store the deserialized header data in.
                    If this is <b>NULL</b>, then the message heap will be used
                    as required by the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param value

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param valueSize [in]

The interpretation of this parameter depends on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a>.

### -param headerAttributes

Returns the <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_text_type">WS_HEADER_ATTRIBUTES</a> for this header.
                    The pointer may be <b>NULL</b>, in which case no attributes are returned.

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
                


<a href="/windows/desktop/api/webservices/ne-webservices-ws_repeating_header_option">WS_SINGLETON_HEADER</a> was specified, and there are 
                    multiple instances of the type of header present in the message.
                

The input data was not in the expected format.
                

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

This API operates on headers targeted at the ultimate receiver.  
                Headers targeted with a role/actor other than ultimate receiver are 
                ignored by this API.