---
UID: NC:webservices.WS_GET_CHANNEL_PROPERTY_CALLBACK
title: WS_GET_CHANNEL_PROPERTY_CALLBACK (webservices.h)
description: Handles the WsGetChannelProperty call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_GET_CHANNEL_PROPERTY_CALLBACK","WS_GET_CHANNEL_PROPERTY_CALLBACK callback","WS_GET_CHANNEL_PROPERTY_CALLBACK callback function [Web Services for Windows]","webservices/WS_GET_CHANNEL_PROPERTY_CALLBACK","wsw.ws_get_channel_property_callback"]
old-location: wsw\ws_get_channel_property_callback.htm
tech.root: wsw
ms.assetid: 8fd503a9-6f8d-46c3-9338-c900b9b1d747
ms.date: 12/05/2018
ms.keywords: WS_GET_CHANNEL_PROPERTY_CALLBACK, WS_GET_CHANNEL_PROPERTY_CALLBACK callback, WS_GET_CHANNEL_PROPERTY_CALLBACK callback function [Web Services for Windows], webservices/WS_GET_CHANNEL_PROPERTY_CALLBACK, wsw.ws_get_channel_property_callback
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
 - WS_GET_CHANNEL_PROPERTY_CALLBACK
 - webservices/WS_GET_CHANNEL_PROPERTY_CALLBACK
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
 - WS_GET_CHANNEL_PROPERTY_CALLBACK
---

# WS_GET_CHANNEL_PROPERTY_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsgetchannelproperty">WsGetChannelProperty</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param id [in]

The id of the property to retrieve.

### -param value

The location to store the retrieved property.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property id was not supported for this object or the specified buffer was not large enough for the value.

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

See <a href="/windows/desktop/api/webservices/nf-webservices-wsgetchannelproperty">WsGetChannelProperty</a> for information about the contract
                of this API.
            

Every custom channel implementation must support returning
                a value for at least the following properties:
            

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ENVELOPE_VERSION</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_TRANSFER_MODE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_PROTECTION_LEVEL</a>
</li>
</ul>
Service Model layer provides its own logic of call timeouts as such it requires 
                disabling timeouts in the underlying channel. In order for a custom channel to be 
                used from Service Model layer, it should support disabling all of its timeouts and 
                implement this callback for <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ENABLE_TIMEOUTS</a>. A custom 
                channel cannot be used through Service Model unless query for 
                <b>WS_CHANNEL_PROPERTY_ENABLE_TIMEOUTS</b> returns <b>FALSE</b>.
            

It is up to the custom channel implementation to determine any
                additional properties it wishes to support.
            

If a property is not supported, the <b>E_INVALIDARG</b> should be returned.
             (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)
