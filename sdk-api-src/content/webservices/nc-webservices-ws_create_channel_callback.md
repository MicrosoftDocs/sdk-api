---
UID: NC:webservices.WS_CREATE_CHANNEL_CALLBACK
title: WS_CREATE_CHANNEL_CALLBACK (webservices.h)
description: Handles the WsCreateChannel call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_CREATE_CHANNEL_CALLBACK","WS_CREATE_CHANNEL_CALLBACK callback","WS_CREATE_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_CREATE_CHANNEL_CALLBACK","wsw.ws_create_channel_callback"]
old-location: wsw\ws_create_channel_callback.htm
tech.root: wsw
ms.assetid: 440114f9-2258-4c33-93cd-7185ccf36f76
ms.date: 12/05/2018
ms.keywords: WS_CREATE_CHANNEL_CALLBACK, WS_CREATE_CHANNEL_CALLBACK callback, WS_CREATE_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_CREATE_CHANNEL_CALLBACK, wsw.ws_create_channel_callback
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
 - WS_CREATE_CHANNEL_CALLBACK
 - webservices/WS_CREATE_CHANNEL_CALLBACK
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
 - WS_CREATE_CHANNEL_CALLBACK
---

# WS_CREATE_CHANNEL_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelType [in]

The message exchange pattern of the channel.
                

If the type of channel is not supported by the custom
                    channel implementation,  <b>E_INVALIDARG</b> should be returned.

### -param channelParameters

The pointer to the value that was specified by the
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</a> property when the custom channel is created using <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a>.
                

If the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</a> property was not specified, the value will be <b>NULL</b>.

### -param channelParametersSize [in]

The size in bytes of the value pointed to by channelParameters.
                

If the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</a> property was not specified, the size will be 0.
                


#### - **channelInstance

A pointer to a structure allocated by the callback 
                    that contains the data specific to this channel instance.  This pointer
                    will be passed to all the other channel callbacks
                    for this particular channel instance.
                

If this callback is successful, then the <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_channel_callback">WS_FREE_CHANNEL_CALLBACK</a> will be used to free the channel instance returned
                    in this parameter.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

### -param channelInstance

A pointer to a structure allocated by the callback 
                    that contains the data specific to this channel instance.  This pointer
                    will be passed to all the other channel callbacks
                    for this particular channel instance.
                

If this callback is successful, then the <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_channel_callback">WS_FREE_CHANNEL_CALLBACK</a> will be used to free the channel instance returned
                    in this parameter.

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
One or more arguments are invalid.

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
