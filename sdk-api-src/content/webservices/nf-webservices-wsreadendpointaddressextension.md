---
UID: NF:webservices.WsReadEndpointAddressExtension
title: WsReadEndpointAddressExtension function (webservices.h)
description: Reads an extension of the WS_ENDPOINT_ADDRESS.
helpviewer_keywords: ["WsReadEndpointAddressExtension","WsReadEndpointAddressExtension function [Web Services for Windows]","webservices/WsReadEndpointAddressExtension","wsw.wsreadendpointaddressextension"]
old-location: wsw\wsreadendpointaddressextension.htm
tech.root: wsw
ms.assetid: 6133be54-8d47-4869-bf84-892324175942
ms.date: 12/05/2018
ms.keywords: WsReadEndpointAddressExtension, WsReadEndpointAddressExtension function [Web Services for Windows], webservices/WsReadEndpointAddressExtension, wsw.wsreadendpointaddressextension
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
 - WsReadEndpointAddressExtension
 - webservices/WsReadEndpointAddressExtension
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
 - WsReadEndpointAddressExtension
---

# WsReadEndpointAddressExtension function


## -description

Reads an extension of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a>.

## -parameters

### -param reader [in]

The XML reader to use to read the extension.
                

The function will automatically set the input of
                    the reader as necessary to read the extensions.

### -param endpointAddress [in]

The endpoint address containing the extensions.

### -param extensionType [in]

The type of extension to read.

### -param readOption [in]

Whether the value is required, and how to allocate the value.
                    See <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTION</a> for more information.
                

This parameter must have one of the following values:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_VALUE</a>.
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_POINTER</a>.
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTIONAL_POINTER</a>.
                </li>
</ul>

### -param heap [in]

The heap to use to store the value that is read.

### -param value

The address of a buffer to place the value read.
                

If using <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_VALUE</a> for the readOption
                    parameter, the buffer must be the size of the type of extension
                    being read (which varies by <a href="/windows/desktop/api/webservices/ne-webservices-ws_endpoint_address_extension_type">WS_ENDPOINT_ADDRESS_EXTENSION_TYPE</a>).
                

If using <a href="/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_POINTER</a> or <b>WS_READ_OPTIONAL_POINTER</b>,
                    the buffer should be the size of a pointer.

### -param valueSize [in]

The size of the buffer that the caller has allocated for the value read.
                

This size should correspond to the size of the buffer passed
                    using the value parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The extension type was not valid.

The size of the supplied buffer was not correct.

A required parameter was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

The returned value is valid until the heap is freed or reset.
            

If the requested extension type appears more than once in the
                extensions buffer, then the first instance is returned.