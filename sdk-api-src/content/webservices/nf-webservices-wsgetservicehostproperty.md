---
UID: NF:webservices.WsGetServiceHostProperty
title: WsGetServiceHostProperty function (webservices.h)
description: Retrieves a specified Service Host property. The property to retrieve is identified by a WS_SERVICE_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetServiceHostProperty","WsGetServiceHostProperty function [Web Services for Windows]","webservices/WsGetServiceHostProperty","wsw.wsgetservicehostproperty"]
old-location: wsw\wsgetservicehostproperty.htm
tech.root: wsw
ms.assetid: 3793cb79-37b9-4d94-9932-9eb3b259b60e
ms.date: 12/05/2018
ms.keywords: WsGetServiceHostProperty, WsGetServiceHostProperty function [Web Services for Windows], webservices/WsGetServiceHostProperty, wsw.wsgetservicehostproperty
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
 - WsGetServiceHostProperty
 - webservices/WsGetServiceHostProperty
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
 - WsGetServiceHostProperty
---

# WsGetServiceHostProperty function


## -description

Retrieves a specified Service Host property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_property_id">WS_SERVICE_PROPERTY_ID</a> input parameter.

## -parameters

### -param serviceHost [in]

A pointer to the WS_SERVICE_HOST object containing the property to retrieve.

### -param id [in]

This is a <b>WS_SERVICE_PROPERTY_ID</b> enumerator value that identifies the property to retrieve.

### -param value

A void pointer to a location for storing the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The byte-length buffer size allocated by the caller to store the retrieved property value.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

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
The property id was not supported for this object or the specified buffer was not large enough for the value.

</td>
</tr>
</table>