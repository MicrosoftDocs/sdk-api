---
UID: NF:webservices.WsSetListenerProperty
title: WsSetListenerProperty function (webservices.h)
description: Sets a Listenerobject property.
helpviewer_keywords: ["WsSetListenerProperty","WsSetListenerProperty function [Web Services for Windows]","webservices/WsSetListenerProperty","wsw.wssetlistenerproperty"]
old-location: wsw\wssetlistenerproperty.htm
tech.root: wsw
ms.assetid: 5c494651-3944-4424-8cd4-a6e14c239e80
ms.date: 12/05/2018
ms.keywords: WsSetListenerProperty, WsSetListenerProperty function [Web Services for Windows], webservices/WsSetListenerProperty, wsw.wssetlistenerproperty
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
 - WsSetListenerProperty
 - webservices/WsSetListenerProperty
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
 - WsSetListenerProperty
---

# WsSetListenerProperty function


## -description

Sets a Listenerobject property.

## -parameters

### -param listener [in]

A pointer to the <b>Listener</b> object with the property to set.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> and may not be <b>NULL</b>.

### -param id [in]

Identifier of the property to set.

### -param value

A void pointer to the property value to set.
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