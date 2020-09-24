---
UID: NF:webservices.WsGetSecurityContextProperty
title: WsGetSecurityContextProperty function (webservices.h)
description: Gets a property of the specified security context.
helpviewer_keywords: ["WsGetSecurityContextProperty","WsGetSecurityContextProperty function [Web Services for Windows]","webservices/WsGetSecurityContextProperty","wsw.wsgetsecuritycontextproperty"]
old-location: wsw\wsgetsecuritycontextproperty.htm
tech.root: wsw
ms.assetid: 7ef32fbe-0b50-4ede-96af-075137df340d
ms.date: 12/05/2018
ms.keywords: WsGetSecurityContextProperty, WsGetSecurityContextProperty function [Web Services for Windows], webservices/WsGetSecurityContextProperty, wsw.wsgetsecuritycontextproperty
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
 - WsGetSecurityContextProperty
 - webservices/WsGetSecurityContextProperty
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
 - WsGetSecurityContextProperty
---

# WsGetSecurityContextProperty function


## -description

Gets a property of the specified security context.

## -parameters

### -param securityContext [in]

The security context that is queried for its property.

### -param id [in]

The id of the property (one of <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_context_property_id">WS_SECURITY_CONTEXT_PROPERTY_ID</a>).

### -param value

The address to place the retrieved value. The pointer must have an alignment compatible with the type of the property.

### -param valueSize [in]

The size of the buffer that the caller has allocated for the retrieved value.

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