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

# WsGetWriterProperty function


## -description


Retrieves a specified XML Writer property.  The property to retrieve is identified by a  <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML WRITER_PROPERTY_ID</a> input parameter.
            


## -parameters




### -param writer [in]


                    A pointer  to a WS_XML_WRITER structure that contains the property value to retrieve.  


### -param id [in]

This is a <b>WS_XML_WRITER_PROPERTY_ID</b> enumerator that identifies the property to retrieve.
                


### -param value

A void pointer to a location for storing the retrieved property value.
                    


### -param valueSize [in]

The byte-length buffer size allocated by the caller to store the retrieved property value.
                The pointer must have an alignment compatible with the type
            of the property.
        


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
 



