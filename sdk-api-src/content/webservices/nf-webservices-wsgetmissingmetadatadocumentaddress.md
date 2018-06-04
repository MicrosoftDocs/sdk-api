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

# WsGetMissingMetadataDocumentAddress function


## -description



                This function returns the address of a missing document that is referenced by the metadata object.
            


                Each document that is added to the metadata object may contain references to
                other documents.    After a document has been added
                back to the Metadata the function can be used to find the next missing document.
            
<div class="alert"><b>Note</b>  This function will fail if the host name of the URL of the missing address 
                being returned cannot be verified as being one of the host names expected.
                The expected host names are a union of the following:
            <ul>
<li>The host name of any URL previously passed to <a href="https://msdn.microsoft.com/0b824948-e06d-482d-8d53-c4e27d1ecf0f">WsReadMetadata</a>.
                </li>
<li>The list of host names specified using the <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_HOST_NAMES</a> property.
            </li>
</ul>
</div><div> </div>

## -parameters




### -param metadata [in]


                    This parameter is a pointer to a <b>Metadata</b> object that should have the document.  


### -param address

On success this parameter is populated with either a pointer to the 
                    address of a missing metadata document, or <b>NULL</b> if there are no missing 
                    metadata documents.
                
                    The returned address URL is fully qualified.
                

<div class="alert"><b>Note</b>  
                    The data returned by this function is valid until the metadata
                    object is freed or reset.  The data should not be modified.
                </div>
<div> </div>



### -param error [in, optional]

This parameter is a  <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> pointer to where additional information about the error should be stored if the function fails.
                


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
 




## -remarks




                Whether or not this function will verify host names of URLs returned can be
                controlled using the <b>WS_METADATA_PROPERTY_VERIFY_HOST_NAMES</b> enumerator value.
            


                The purpose of the host name verification is to ensure that an application
                does not use the address without knowing that it is from a host that it 
                is willing to accept metadata from.
            



