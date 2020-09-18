---
UID: NF:webservices.WsGetChannelProperty
title: WsGetChannelProperty function (webservices.h)
description: Retrieves a property of the Channel referenced by the channel parameter.
helpviewer_keywords: ["WsGetChannelProperty","WsGetChannelProperty function [Web Services for Windows]","webservices/WsGetChannelProperty","wsw.wsgetchannelproperty"]
old-location: wsw\wsgetchannelproperty.htm
tech.root: wsw
ms.assetid: 6f3440d2-90cc-4312-bb08-51f08b864cc7
ms.date: 12/05/2018
ms.keywords: WsGetChannelProperty, WsGetChannelProperty function [Web Services for Windows], webservices/WsGetChannelProperty, wsw.wsgetchannelproperty
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
 - WsGetChannelProperty
 - webservices/WsGetChannelProperty
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
 - WsGetChannelProperty
---

# WsGetChannelProperty function


## -description

Retrieves a property of the Channel referenced by the <i>channel</i> parameter.

## -parameters

### -param channel [in]

A pointer to the  <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> object with the property to retrieve.

### -param id [in]

Represents an identifier of the property to retrieve.

### -param value

A void pointer referencing the location to store the retrieved property.
                    <div class="alert"><b>Note</b>  The pointer must have an alignment compatible with the type
                    of the property.
                </div>
<div> </div>

### -param valueSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.

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
The property Id was not supported for this object or the specified buffer was not large enough.

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