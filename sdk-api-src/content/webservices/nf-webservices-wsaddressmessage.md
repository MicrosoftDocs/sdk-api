---
UID: NF:webservices.WsAddressMessage
title: WsAddressMessage function (webservices.h)
description: Addresses a message to a specified endpoint address.
helpviewer_keywords: ["WsAddressMessage","WsAddressMessage function [Web Services for Windows]","webservices/WsAddressMessage","wsw.wsaddressmessage"]
old-location: wsw\wsaddressmessage.htm
tech.root: wsw
ms.assetid: 30b2dbd1-7232-4ff1-b30a-920df8bfe423
ms.date: 12/05/2018
ms.keywords: WsAddressMessage, WsAddressMessage function [Web Services for Windows], webservices/WsAddressMessage, wsw.wsaddressmessage
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
 - WsAddressMessage
 - webservices/WsAddressMessage
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
 - WsAddressMessage
---

# WsAddressMessage function


## -description

Addresses a <a href="/windows/desktop/wsw/message">message</a> to a specified <a href="/windows/desktop/wsw/endpoint-address">endpoint address</a>.

## -parameters

### -param message [in]

Pointer to a <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> structure representing the  message to be addressed.

### -param address [in, optional]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> structure containing the endpoint  to which to address the message.

<div class="alert"><b>Note</b>  Passing <b>NULL</b> to this parameter indicates that no headers are added to the message.  This provides
                    a way to set the <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_ID</a> to <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> 
                    without modifying the set of headers in the message.
                </div>
<div> </div>

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The message has already been addressed.
                    (The <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> property
                    indicates whether a message has already been addressed.)
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

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
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function can return other errors not listed above.

</td>
</tr>
</table>

## -remarks

If you do not address a message by calling  this function, the <a href="/windows/desktop/wsw/channel">channel</a> automatically addresses the message with the
                <a href="/windows/desktop/wsw/endpoint-address">Endpoint Address</a> passed to <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">WsOpenChannel</a>.

This function marks the message as addressed by setting
                the  <b>WS_MESSAGE_PROPERTY_IS_ADDRESSED</b> property  to <b>TRUE</b>.
            

This function fails 
                if the message has already been addressed and returns <b>WS_E_INVALID_OPERATION</b>.
            

If a non-<b>NULL</b><a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> is passed
                to the function,  the function performs the following
                additional steps:
            

<ul>
<li>The header type is set to WS_TO_HEADER (see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_header_type">WS_HEADER_TYPE</a> enumeration) and the address is set to the value of the <b>url</b> field of <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a>.  If the URL length
                is zero the <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION</a>-specific 
                representation for an anonymous URL is set for the message.
                </li>
<li>Each header in the <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> specified in the 
                headers field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> is added to
                the message.  No headers are added if the buffer is <b>NULL</b>.
            </li>
</ul>