---
UID: NF:webservices.WsGetSecurityTokenProperty
title: WsGetSecurityTokenProperty function (webservices.h)
description: Extracts a field or a property from a security token.
helpviewer_keywords: ["WsGetSecurityTokenProperty","WsGetSecurityTokenProperty function [Web Services for Windows]","webservices/WsGetSecurityTokenProperty","wsw.wsgetsecuritytokenproperty"]
old-location: wsw\wsgetsecuritytokenproperty.htm
tech.root: wsw
ms.assetid: ce41062f-5125-4a4b-acc1-5df15b26276b
ms.date: 12/05/2018
ms.keywords: WsGetSecurityTokenProperty, WsGetSecurityTokenProperty function [Web Services for Windows], webservices/WsGetSecurityTokenProperty, wsw.wsgetsecuritytokenproperty
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
 - WsGetSecurityTokenProperty
 - webservices/WsGetSecurityTokenProperty
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
 - WsGetSecurityTokenProperty
---

# WsGetSecurityTokenProperty function


## -description

Extracts a field or a property from a security token. If the queried property does not use the <i>heap</i> parameter, the returned data is owned by the security token and remains valid as long as the security token itself remains valid. Specifically, for security tokens extracted from a received message, the security token and fields extracted from it are valid only as long as the message is not reset or freed. 

If the <i>heap</i> parameter is required by the property, then the returned data is stored on the heap, with its lifetime detached from the underlying token.

## -parameters

### -param securityToken [in]

The security token from which the property should be extracted.

### -param id [in]

The id of the property to retrieve.

### -param value

The location to store the retrieved property.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.

### -param heap [in, optional]

Heap to store additional property data. This parameter must be non-<b>NULL</b> when the queried property is
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_token_property_id">WS_SECURITY_TOKEN_PROPERTY_SYMMETRIC_KEY</a> and must be <b>NULL</b> otherwise.

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