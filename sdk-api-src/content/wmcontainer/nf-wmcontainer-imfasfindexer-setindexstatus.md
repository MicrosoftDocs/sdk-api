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

# IMFASFIndexer::SetIndexStatus


## -description



Configures the index for a stream.




## -parameters




### -param pbIndexDescriptor




### -param cbIndexDescriptor [in]

The size, in bytes, of the index descriptor.


### -param fGenerateIndex [in]

A Boolean value. Set to <b>TRUE</b> to have the indexer create an index of the type specified for the stream specified in the index descriptor.


#### - pIndexDescriptor [in]

The index descriptor to set. The index descriptor is an <a href="https://msdn.microsoft.com/2a540aef-068d-4465-b0ed-64aed828af01">ASF_INDEX_DESCRIPTOR</a> structure, optionally followed by index-specific data.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
At attempt was made to change the index status in a seek-only scenario. For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



You must make all calls to <b>SetIndexStatus</b> before making any calls to <a href="https://msdn.microsoft.com/febc5335-a8e8-4ae9-afb2-17f09b750477">IMFASFIndexer::GenerateIndexEntries</a>.

The indexer object is configured to create temporal indexes for each stream by default. Call this method only if you want to override the default settings.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

