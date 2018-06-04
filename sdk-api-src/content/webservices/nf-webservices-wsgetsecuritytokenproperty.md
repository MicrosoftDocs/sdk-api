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

# WsGetSecurityTokenProperty function


## -description


Extracts a field or a property from a security token. If the queried property does not use the <i>heap</i> parameter, the returned data is owned by the security token and remains valid as long as the security token itself remains valid. Specifically, for security tokens extracted from a received message, the security token and fields extracted from it are valid only as long as the message is not reset or freed. 

If the <i>heap</i> parameter is required by the property, then the returned data is stored on the heap, with its lifetime detached from the underlying token. 




## -parameters




### -param securityToken [in]


The security token from which the property should be extracted.
                


### -param id [in]


The id of the property to retrieve.
                


### -param value


                    The location to store the retrieved property.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]


                    The number of bytes allocated by the caller to
                    store the retrieved property.
                


### -param heap [in, optional]


                    Heap to store additional property data. This parameter must be non-<b>NULL</b> when the queried property is
                    <a href="https://msdn.microsoft.com/d5ba0170-2345-4144-9a60-25c0e638a283">WS_SECURITY_TOKEN_PROPERTY_SYMMETRIC_KEY</a> and must be <b>NULL</b> otherwise.
                


### -param error [in, optional]


Specifies where additional error information should be stored if the function fails.
                


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
 



