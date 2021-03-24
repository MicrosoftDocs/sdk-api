---
UID: NF:webservices.WsCreateServiceProxy
title: WsCreateServiceProxy function (webservices.h)
description: Creates a service proxy with the specified properties.
helpviewer_keywords: ["WsCreateServiceProxy","WsCreateServiceProxy function [Web Services for Windows]","webservices/WsCreateServiceProxy","wsw.wscreateserviceproxy"]
old-location: wsw\wscreateserviceproxy.htm
tech.root: wsw
ms.assetid: 9215684b-979e-48ad-b4ee-2ae1db1e3034
ms.date: 12/05/2018
ms.keywords: WsCreateServiceProxy, WsCreateServiceProxy function [Web Services for Windows], webservices/WsCreateServiceProxy, wsw.wscreateserviceproxy
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
 - WsCreateServiceProxy
 - webservices/WsCreateServiceProxy
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
 - WsCreateServiceProxy
---

# WsCreateServiceProxy function


## -description

Creates a  <a href="/windows/desktop/wsw/service-proxy">service proxy</a> with the specified properties.

## -parameters

### -param channelType [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE</a> enumeration value representing the channel type for the service proxy.

### -param channelBinding [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> enumeration value representing the channel binding.

### -param securityDescription [in, optional]

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">WS_SECURITY_DESCRIPTION</a> structure representing the security description.

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_proxy_property">WS_PROXY_PROPERTY</a> structures containing optional properties for the service proxy.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param channelProperties

An array of  <a href="/windows/desktop/api/webservices/ns-webservices-ws_channel_property">WS_CHANNEL_PROPERTY</a>  structures containing optional channel properties.  The value of this parameter may be <b>NULL</b>, in which case, the <i>channelPropertyCount</i> parameter must be 0 (zero).
                

<div class="alert"><b>Note</b>  Be very careful about modifying the default values for these properties.</div>
<div> </div>

### -param channelPropertyCount [in]

The number of properties in the <i>channelProperties</i> array.

### -param serviceProxy

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> structure representing the new service proxy.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeserviceproxy">WsFreeServiceProxy</a>.

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