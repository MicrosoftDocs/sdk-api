---
UID: NF:webservices.WsGetMessageProperty
title: WsGetMessageProperty function (webservices.h)
description: Retrieves a specified Message object property. The property to retrieve is identified by a WS_MESSAGE_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetMessageProperty","WsGetMessageProperty function [Web Services for Windows]","webservices/WsGetMessageProperty","wsw.wsgetmessageproperty"]
old-location: wsw\wsgetmessageproperty.htm
tech.root: wsw
ms.assetid: 369f7690-6d70-401a-84aa-e5761dc874b5
ms.date: 12/05/2018
ms.keywords: WsGetMessageProperty, WsGetMessageProperty function [Web Services for Windows], webservices/WsGetMessageProperty, wsw.wsgetmessageproperty
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
 - WsGetMessageProperty
 - webservices/WsGetMessageProperty
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
 - WsGetMessageProperty
---

# WsGetMessageProperty function


## -description

Retrieves a specified Message object  property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_ID</a> input parameter.

## -parameters

### -param message [in]

A pointer to a <b>Message</b> object containing the desired property.  This parameter must be a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> object.

### -param id [in]

This is a <b>WS_MESSAGE_PROPERTY_ID</b> enumerator value that identifies the desired property.

### -param value

A reference to a location for storing the retrieved property value.
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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The application has run out of memory.

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