---
UID: NF:webservices.WsGetMetadataEndpoints
title: WsGetMetadataEndpoints function (webservices.h)
description: Returns the &quot;Endpoints&quot; defined within the metadata object documents.
helpviewer_keywords: ["WsGetMetadataEndpoints","WsGetMetadataEndpoints function [Web Services for Windows]","webservices/WsGetMetadataEndpoints","wsw.wsgetmetadataendpoints"]
old-location: wsw\wsgetmetadataendpoints.htm
tech.root: wsw
ms.assetid: 1cf9f2ba-c303-4668-a959-8fad69746438
ms.date: 12/05/2018
ms.keywords: WsGetMetadataEndpoints, WsGetMetadataEndpoints function [Web Services for Windows], webservices/WsGetMetadataEndpoints, wsw.wsgetmetadataendpoints
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
 - WsGetMetadataEndpoints
 - webservices/WsGetMetadataEndpoints
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
 - WsGetMetadataEndpoints
---

# WsGetMetadataEndpoints function


## -description

Returns the "Endpoints" defined within the metadata object documents.
            Calling this function with <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_state">WS_METADATA_STATE</a>set to <b>WS_METADATA_STATE_CREATED</b> will cause the metadata object to resolve
                all references in the metadata documents. Any
                additional document validation will also be done.  If this process is
                successful  the metadata object will be set to <b>WS_METADATA_STATE_RESOLVED</b> and  subsequent document additions to the metadata object are not permitted.   If there is an error the metadata object 
                will be set to <b>WS_METADATA_STATE_FAULTED</b>.
            
<div class="alert"><b>Note</b>  The data returned by this function is valid until the metadata
                object is released or reset.  The data returned from this function
                should not be modified.
            </div><div> </div>

## -parameters

### -param metadata [in]

A pointer to a <b>Metadata</b> object containing the desired Endpoints.  This parameter must be a valid <a href="/windows/desktop/wsw/ws-metadata">WS_METADATA</a> object.

### -param endpoints [out]

On success this pointer parameter 
                    is populated with information about the endpoints that were 
                    defined in the metadata object.

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
Insufficient memory resources.

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

## -remarks

This property may be used in <b>WS_METADATA_STATE_CREATED</b> or <b>WS_METADATA_STATE_RESOLVED</b> state.
            

This function will fail if there are missing metadata documents.
                Use <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmissingmetadatadocumentaddress">WsGetMissingMetadataDocumentAddress</a> to determine
                the address of any missing documents.