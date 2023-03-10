---
UID: NF:webservices.WsGetServiceProxyProperty
title: WsGetServiceProxyProperty function (webservices.h)
description: This function retrieves a specified Service Proxy property. The property to retrieve is identified by a WS_PROXY_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetServiceProxyProperty","WsGetServiceProxyProperty function [Web Services for Windows]","webservices/WsGetServiceProxyProperty","wsw.wsgetserviceproxyproperty"]
old-location: wsw\wsgetserviceproxyproperty.htm
tech.root: wsw
ms.assetid: 4fb4124f-5beb-426a-890f-3a8fe236411f
ms.date: 12/05/2018
ms.keywords: WsGetServiceProxyProperty, WsGetServiceProxyProperty function [Web Services for Windows], webservices/WsGetServiceProxyProperty, wsw.wsgetserviceproxyproperty
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
 - WsGetServiceProxyProperty
 - webservices/WsGetServiceProxyProperty
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
 - WsGetServiceProxyProperty
---

# WsGetServiceProxyProperty function


## -description

This function retrieves a specified Service Proxy property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ne-webservices-ws_proxy_property_id">WS_PROXY_PROPERTY_ID</a> input parameter.

## -parameters

### -param serviceProxy [in]

This parameter is a pointer to the WS_SERVICE_PROXY object containing the property to retrieve.

### -param id [in]

The value of this parameter is a <b>WS_PROXY_PROPERTY_ID</b> enumerator value that identifies the property to retrieve.

### -param value

This parameter is a reference to a location for storing the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The value of this ULONG parameter represents the byte-length buffer size allocated by the caller to store the retrieved property value.

### -param error [in, optional]

This parameter is a  <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> pointer to where additional information about the error should be stored if the function fails.

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
The property id was not supported for this object.

</td>
</tr>
</table>