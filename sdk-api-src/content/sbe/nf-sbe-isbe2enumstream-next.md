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

# ISBE2EnumStream::Next


## -description



        Retrieves the next <i>n</i> streams in the collection.
      


## -parameters




### -param cRequest [in]

The number of streams to retrieve.




### -param pStreamDesc [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/ab7ccd5b-1ac8-4d33-aea6-49383025270b">SBE2_STREAM_DESC</a> structures, with at least <i>cRequest</i> elements. The method copies up to <i>cRequest</i> elements into the array.


### -param pcReceived [out]

Receives the number of elements returned in the <i>pStreamDesc</i> array. This parameter can be <b>NULL</b> if <i>cRequest</i> is 1.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded and retrieved <i>cRequest</i> elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The method retrieved fewer elements than requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The streams have changed, so the caller must enumerate them again.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>
 

 

