---
UID: NF:webservices.WsGetListenerProperty
title: WsGetListenerProperty function (webservices.h)
description: Retrieves a specified Listener object property. The property to retrieve is identified by a WS_LISTENER_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetListenerProperty","WsGetListenerProperty function [Web Services for Windows]","webservices/WsGetListenerProperty","wsw.wsgetlistenerproperty"]
old-location: wsw\wsgetlistenerproperty.htm
tech.root: wsw
ms.assetid: cc4fb48a-8282-471a-aed0-1ca3134f9bd0
ms.date: 12/05/2018
ms.keywords: WsGetListenerProperty, WsGetListenerProperty function [Web Services for Windows], webservices/WsGetListenerProperty, wsw.wsgetlistenerproperty
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
 - WsGetListenerProperty
 - webservices/WsGetListenerProperty
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
 - WsGetListenerProperty
---

# WsGetListenerProperty function


## -description

Retrieves a specified Listener object  property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ns-webservices-ws_listener_property">WS_LISTENER_PROPERTY_ID</a> input parameter.

## -parameters

### -param listener [in]

A pointer to the Listener object containing the desired property.  This must be a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> that was returned
                    from <a href="/windows/desktop/api/webservices/nf-webservices-wscreatelistener">WsCreateListener</a>.

### -param id [in]

This is a <b>WS_LISTENER_PROPERTY_ID</b> enumerator value that identifies the desired property.

### -param value

A reference to a location for storing the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

Represents the byte-length buffer size allocated by the caller to store the retrieved property value.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>