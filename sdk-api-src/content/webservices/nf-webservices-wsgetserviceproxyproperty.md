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

# WsGetServiceProxyProperty function


## -description


This function retrieves a specified Service Proxy property.  The property to retrieve is identified by a  <a href="https://msdn.microsoft.com/d81944ae-74b9-4eee-b02f-5b1d5c99c358">WS_PROXY_PROPERTY_ID</a> input parameter.
            


## -parameters




### -param serviceProxy [in]


                    This parameter is a pointer to the WS_SERVICE_PROXY object containing the property to retrieve.  


### -param id [in]

The value of this parameter is a <b>WS_PROXY_PROPERTY_ID</b> enumerator value that identifies the property to retrieve.
                


### -param value

This parameter is a reference to a location for storing the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The value of this ULONG parameter represents the byte-length buffer size allocated by the caller to store the retrieved property value.
                


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
The property id was not supported for this object.

</td>
</tr>
</table>
 



