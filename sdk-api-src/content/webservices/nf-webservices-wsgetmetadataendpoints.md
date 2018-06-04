---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WsGetMetadataEndpoints function


## -description


Returns the "Endpoints" defined within the metadata object documents.
            Calling this function with <a href="https://msdn.microsoft.com/4d2b8c31-d5ff-4b96-9aaf-57e59d075431">WS_METADATA_STATE</a>
                 set to <b>WS_METADATA_STATE_CREATED</b> will cause the metadata object to resolve
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

A pointer to a <b>Metadata</b> object containing the desired Endpoints.  This parameter must be a valid <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a> object.  


### -param endpoints [out]

On success this pointer parameter 
                    is populated with information about the endpoints that were 
                    defined in the metadata object.
                


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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




                This property may be used in <b>WS_METADATA_STATE_CREATED</b>
                or <b>WS_METADATA_STATE_RESOLVED</b> state.
            


                This function will fail if there are missing metadata documents.
                Use <a href="https://msdn.microsoft.com/7854fb44-c397-4fd0-8a0e-ea293eba4f01">WsGetMissingMetadataDocumentAddress</a> to determine
                the address of any missing documents.
            



