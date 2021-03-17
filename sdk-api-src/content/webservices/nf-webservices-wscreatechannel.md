---
UID: NF:webservices.WsCreateChannel
title: WsCreateChannel function (webservices.h)
description: Creates a channel for message exchange with an endpoint.
helpviewer_keywords: ["WsCreateChannel","WsCreateChannel function [Web Services for Windows]","webservices/WsCreateChannel","wsw.wscreatechannel"]
old-location: wsw\wscreatechannel.htm
tech.root: wsw
ms.assetid: 4bef6f97-06f1-442a-8b84-869776f0541d
ms.date: 12/05/2018
ms.keywords: WsCreateChannel, WsCreateChannel function [Web Services for Windows], webservices/WsCreateChannel, wsw.wscreatechannel
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
 - WsCreateChannel
 - webservices/WsCreateChannel
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
 - WsCreateChannel
---

# WsCreateChannel function


## -description

Creates a <a href="/windows/desktop/wsw/channel">channel</a> for message exchange with an endpoint.

## -parameters

### -param channelType [in]

The type of the channel. For channel types, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE</a> enumeration. This represents the message exchange pattern for the channel being created.

### -param channelBinding [in]

The channel <a href="/windows/desktop/wsw/binding">binding</a>, indicating the protocol stack to use for the new channel.
                For available channel bindings, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> enumeration.

### -param properties [in]

An array of  <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_property">WS_CHANNEL_PROPERTY</a>  structures  containing optional values for channel initialization.  The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For information on which channel properties can be specified when you create a channel, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ID</a> enumeration.

For information on creating a custom channel, see the Remarks section.

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param securityDescription [in, optional]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">WS_SECURITY_DESCRIPTION</a>  structure specifying the security for the channel.

If you are creating a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> enumeration), the security description must be <b>NULL</b>. See the Remarks section.

### -param channel

Pointer that receives the address of the created channel.   
                    When the channel  is no longer needed, you must free  it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">WsFreeChannel</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure that receives additional error information if the function fails.

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
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

Use the <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">WsOpenChannel</a> function to initiate  communication on the channel and to specify the endpoint.
            

When you create a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> enumeration), you can specify only the following channel properties: 

<ul>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS </li>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</li>
</ul>(See the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ID</a> enumeration) If initial properties are required to create the custom channel, specify them by using the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS property. 



To pass security information to a custom channel implementation, use the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS value of the  <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ID</a> enumeration.