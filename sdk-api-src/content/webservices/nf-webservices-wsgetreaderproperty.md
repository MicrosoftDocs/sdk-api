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

# WsGetReaderProperty function


## -description


This function returns a property of the specified XML Reader.
<div class="alert"><b>Note</b>  Obtaining the Property <b>WS_XML_READER_PROPERTY_CHARSET</b> will require inspecting up to the first
        four bytes of the XML data.  Consequently if the Reader is using <a href="https://msdn.microsoft.com/53537eb2-6b8d-443e-9453-4b39dfef1dd7">WS_XML_READER_STREAM_INPUT</a> the
        <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a> function must be called first to ensure that this data has been read.</div><div> </div>

## -parameters




### -param reader [in]

A pointer to a WS_XML_READER object containing the desired property value.


### -param id [in]

An enumerator value identifier of the Reader property.
        


### -param value

A pointer to the address for returning the retrieved value.
            The pointer must have an alignment compatible with the type
            of the property.
        


### -param valueSize [in]

A byte count of the buffer that the caller has allocated for the retrieved value.
        


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
</table>
 



