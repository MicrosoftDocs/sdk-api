---
UID: NF:webservices.WsCreateMetadata
title: WsCreateMetadata function (webservices.h)
description: Creates a metadata object that is used to collect and process metadata documents.
helpviewer_keywords: ["WsCreateMetadata","WsCreateMetadata function [Web Services for Windows]","webservices/WsCreateMetadata","wsw.wscreatemetadata"]
old-location: wsw\wscreatemetadata.htm
tech.root: wsw
ms.assetid: c3b6f926-331b-46a7-8180-36762abf63d7
ms.date: 12/05/2018
ms.keywords: WsCreateMetadata, WsCreateMetadata function [Web Services for Windows], webservices/WsCreateMetadata, wsw.wscreatemetadata
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
 - WsCreateMetadata
 - webservices/WsCreateMetadata
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
 - WsCreateMetadata
---

# WsCreateMetadata function


## -description

Creates a metadata object that is used to collect and process metadata documents.

## -parameters

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_metadata_property">WS_METADATA_PROPERTY</a> structures containing optional properties for the metadata.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param metadata

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-metadata">WS_METADATA</a> structure representing the new message.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreemetadata">WsFreeMetadata</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
One or more arguments are invalid.

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