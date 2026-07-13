---
UID: NF:webservices.WsGetErrorProperty
title: WsGetErrorProperty function (webservices.h)
description: Retrieves a property of a WS_ERROR object referenced by the error parameter.
helpviewer_keywords: ["WsGetErrorProperty","WsGetErrorProperty function [Web Services for Windows]","webservices/WsGetErrorProperty","wsw.wsgeterrorproperty"]
old-location: wsw\wsgeterrorproperty.htm
tech.root: wsw
ms.assetid: 35a1f4a8-aad6-43ad-81db-b1071a77d5f4
ms.date: 12/05/2018
ms.keywords: WsGetErrorProperty, WsGetErrorProperty function [Web Services for Windows], webservices/WsGetErrorProperty, wsw.wsgeterrorproperty
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
 - WsGetErrorProperty
 - webservices/WsGetErrorProperty
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
 - WsGetErrorProperty
---

# WsGetErrorProperty function


## -description

Retrieves a property of an <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object referenced by the <i>error</i> parameter.

## -parameters

### -param error [in]

A pointer to the  <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object with the property to retrieve.

### -param id [in]

An identifier of the property to retrieve.

### -param buffer

A pointer referencing the location to store the retrieved property.

### -param bufferSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>