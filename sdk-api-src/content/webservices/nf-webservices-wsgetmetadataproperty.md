---
UID: NF:webservices.WsGetMetadataProperty
title: WsGetMetadataProperty function (webservices.h)
description: Retrieves a specified WS_METADATA object property. The property to retrieve is identified by a WS_METADATA_PROPERTY_ID input parameter.
helpviewer_keywords: ["WsGetMetadataProperty","WsGetMetadataProperty function [Web Services for Windows]","webservices/WsGetMetadataProperty","wsw.wsgetmetadataproperty"]
old-location: wsw\wsgetmetadataproperty.htm
tech.root: wsw
ms.assetid: 21d8dbca-e8a5-4b2f-a1f7-951532922024
ms.date: 12/05/2018
ms.keywords: WsGetMetadataProperty, WsGetMetadataProperty function [Web Services for Windows], webservices/WsGetMetadataProperty, wsw.wsgetmetadataproperty
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
 - WsGetMetadataProperty
 - webservices/WsGetMetadataProperty
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
 - WsGetMetadataProperty
---

# WsGetMetadataProperty function


## -description

Retrieves a specified <a href="/windows/desktop/wsw/ws-metadata">WS_METADATA</a> object  property.  The property to retrieve is identified by a  <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_property_id">WS_METADATA_PROPERTY_ID</a> input parameter.
            
<div class="alert"><b>Note</b>  The data returned by this function is valid until the metadata
                object is released or reset.  The data should not be modified.
            </div><div> </div>

## -parameters

### -param metadata [in]

A pointer to a <b>Metadata</b> object containing the desired property.  This parameter must be a valid <a href="/windows/desktop/wsw/ws-metadata">WS_METADATA</a> object.

### -param id [in]

Identifier value of the property to retrieve.

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
The property Id was not supported for this object or the specified buffer was not large enough for the value.

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