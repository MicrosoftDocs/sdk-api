---
UID: NC:webservices.WS_SET_CHANNEL_PROPERTY_CALLBACK
title: WS_SET_CHANNEL_PROPERTY_CALLBACK (webservices.h)
description: Handles the WsSetChannelProperty call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_SET_CHANNEL_PROPERTY_CALLBACK","WS_SET_CHANNEL_PROPERTY_CALLBACK callback","WS_SET_CHANNEL_PROPERTY_CALLBACK callback function [Web Services for Windows]","webservices/WS_SET_CHANNEL_PROPERTY_CALLBACK","wsw.ws_set_channel_property_callback"]
old-location: wsw\ws_set_channel_property_callback.htm
tech.root: wsw
ms.assetid: 8f7f90dd-0967-4caf-a781-5fc9c588238d
ms.date: 12/05/2018
ms.keywords: WS_SET_CHANNEL_PROPERTY_CALLBACK, WS_SET_CHANNEL_PROPERTY_CALLBACK callback, WS_SET_CHANNEL_PROPERTY_CALLBACK callback function [Web Services for Windows], webservices/WS_SET_CHANNEL_PROPERTY_CALLBACK, wsw.ws_set_channel_property_callback
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
 - WS_SET_CHANNEL_PROPERTY_CALLBACK
 - webservices/WS_SET_CHANNEL_PROPERTY_CALLBACK
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
 - WS_SET_CHANNEL_PROPERTY_CALLBACK
---

# WS_SET_CHANNEL_PROPERTY_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wssetchannelproperty">WsSetChannelProperty</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param id [in]

The id of the property to set.

### -param value

The pointer to the property value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The size of the property value.

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
The property id was not supported for this object.

The specified size was not appropriate for the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough space to set the property value.

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

See <a href="/windows/desktop/api/webservices/nf-webservices-wssetchannelproperty">WsSetChannelProperty</a> for information about the contract
                of this API.
            

It is up to the custom channel implementation to determine the
                set of properties it wishes to support.
            

If a property is not supported, the <b>E_INVALIDARG </b> should be returned.
            (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)
