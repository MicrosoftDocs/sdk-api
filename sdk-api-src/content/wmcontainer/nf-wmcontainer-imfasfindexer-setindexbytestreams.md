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

# IMFASFIndexer::SetIndexByteStreams


## -description



Adds byte streams to be indexed.




## -parameters




### -param ppIByteStreams [in]

An array of <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface pointers. To get the byte stream, call <a href="https://msdn.microsoft.com/edcce9d4-9296-4b39-8e58-58ae602c250f">MFCreateASFIndexerByteStream</a>.


### -param cByteStreams [in]

The number of pointers in the <i>ppIByteStreams</i> array.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The indexer object has already been initialized and it  has packets which have been indexed.

</td>
</tr>
</table>
 




## -remarks



For a reading scenario, only one byte stream should be used by the indexer object. For an index generating scenario, it depends how many index objects are needed to be generated. 




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

