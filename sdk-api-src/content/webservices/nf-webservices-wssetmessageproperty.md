---
UID: NF:webservices.WsSetMessageProperty
title: WsSetMessageProperty function (webservices.h)
description: This operation sets a Messageproperty.
helpviewer_keywords: ["WsSetMessageProperty","WsSetMessageProperty function [Web Services for Windows]","webservices/WsSetMessageProperty","wsw.wssetmessageproperty"]
old-location: wsw\wssetmessageproperty.htm
tech.root: wsw
ms.assetid: f1e6616f-63ac-4afb-90dd-17a776d59eeb
ms.date: 12/05/2018
ms.keywords: WsSetMessageProperty, WsSetMessageProperty function [Web Services for Windows], webservices/WsSetMessageProperty, wsw.wssetmessageproperty
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
 - WsSetMessageProperty
 - webservices/WsSetMessageProperty
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
 - WsSetMessageProperty
---

# WsSetMessageProperty function


## -description

This operation sets a Messageproperty.

## -parameters

### -param message [in]

A pointer to the <b>Message</b> object with the property to set.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-message">WS_MESSAGE</a> object and the referenced value may not be <b>NULL</b>.

### -param id [in]

The identifier of the property to set.

### -param value

A pointer to the property value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.

### -param valueSize [in]

The size in bytes  of the property value.

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
The property id was not supported for this object.

The specified size was not appropriate for the property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough space to set the property value.

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