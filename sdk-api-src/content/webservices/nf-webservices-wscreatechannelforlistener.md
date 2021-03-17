---
UID: NF:webservices.WsCreateChannelForListener
title: WsCreateChannelForListener function (webservices.h)
description: Creates a channel associated with a specified listener.
helpviewer_keywords: ["WsCreateChannelForListener","WsCreateChannelForListener function [Web Services for Windows]","webservices/WsCreateChannelForListener","wsw.wscreatechannelforlistener"]
old-location: wsw\wscreatechannelforlistener.htm
tech.root: wsw
ms.assetid: d9a80506-d891-4cfd-b120-0d3fce946cf5
ms.date: 12/05/2018
ms.keywords: WsCreateChannelForListener, WsCreateChannelForListener function [Web Services for Windows], webservices/WsCreateChannelForListener, wsw.wscreatechannelforlistener
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCreateChannelForListener
 - webservices/WsCreateChannelForListener
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
 - WsCreateChannelForListener
---

# WsCreateChannelForListener function


## -description

Creates a <a href="/windows/desktop/wsw/channel">channel</a> associated with a specified <a href="/windows/desktop/wsw/listener">listener</a>.

## -parameters

### -param listener [in]

Pointer to a <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> structure representing the listener for which to create a channel.  The listener 
                    can be in any state. (For listener states, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_state">WS_LISTENER_STATE</a>  enumeration.)

### -param properties

An array of  <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_property">WS_CHANNEL_PROPERTY</a> structures containing optional values for channel initialization.  This can be a <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                

For information on creating a custom channel, see the Remarks section.

### -param propertyCount [in]

The number of  properties in the <i>properties</i> array.

### -param channel

On success, a pointer that receives the address of the created channel.   
                    When the channel  is no longer needed, you must free  it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">WsFreeChannel</a>.

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

To accept an incoming message exchange, call the <a href="/windows/desktop/api/webservices/nf-webservices-wsacceptchannel">WsAcceptChannel</a> function.
            

The security characteristics of the channel are the same as those 
                specified for the listener.
            

When you create a custom channel (using the WS_CUSTOM_CHANNEL_BINDING value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> enumeration), you can specify only the following channel properties: 

<ul>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS </li>
<li>WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS</li>
</ul>If initial properties are required to create the custom channel, specify them by using the WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_PARAMETERS property.