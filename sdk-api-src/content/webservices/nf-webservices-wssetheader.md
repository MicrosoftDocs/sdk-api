---
UID: NF:webservices.WsSetHeader
title: WsSetHeader function (webservices.h)
description: Adds or replaces the specified standard header in the message.
helpviewer_keywords: ["WsSetHeader","WsSetHeader function [Web Services for Windows]","webservices/WsSetHeader","wsw.wssetheader"]
old-location: wsw\wssetheader.htm
tech.root: wsw
ms.assetid: 34671c47-d21e-47c4-9fb0-10b036fb4f70
ms.date: 12/05/2018
ms.keywords: WsSetHeader, WsSetHeader function [Web Services for Windows], webservices/WsSetHeader, wsw.wssetheader
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
 - WsSetHeader
 - webservices/WsSetHeader
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
 - WsSetHeader
---

# WsSetHeader function


## -description

Adds or replaces the specified standard header in the message.

## -parameters

### -param message [in]

The message to set the header in.
                

The message can be in any state but <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_state">WS_MESSAGE_STATE_EMPTY</a>.

### -param headerType [in]

The type of header to serialize.

### -param valueType [in]

The type of the value to serialize.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a> for
                    the set of types supported for each type of header.

### -param writeOption [in]

Whether the header element is required, and how the value is allocated.
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_NILLABLE_VALUE</a> and <b>WS_WRITE_NILLABLE_POINTER</b> 
                    write options cannot be specified since the header types in <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a> 
                    are not allowed to be nillable in the respective standards specifications.
                    See <b>WS_WRITE_OPTION</b> for more information.

### -param value

The header value to serialize.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_OPTION</a> for
                    more information.

### -param valueSize [in]

The size of the value being serialized, in bytes.

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
There are multiple instances of the type of header present in the message.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to serialize the header.
                

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

This API allows setting of standard header types (see <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a>).
                For application defined header types, use <a href="/windows/desktop/api/webservices/nf-webservices-wsaddcustomheader">WsAddCustomHeader</a>.
            

This API is designed handle types of headers that appear once in the
                message and are targeted at the ultimate receiver.  Headers targeted
                with a role/actor other than ultimate receiver are ignored by this API.
            

If a header of the given type (targeted at the ultimate receiver) already
                exists in the message, it is replaced.