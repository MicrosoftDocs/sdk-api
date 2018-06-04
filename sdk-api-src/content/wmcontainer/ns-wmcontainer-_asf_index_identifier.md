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

# _ASF_INDEX_IDENTIFIER structure


## -description



          Specifies an index for the ASF indexer object.
        


## -struct-fields




### -field guidIndexType


            The type of index. Currently this value must be GUID_NULL, which specifies time-based indexing.
          


### -field wStreamNumber


            The stream number to which this structure applies.
          


## -remarks




        The index object of an ASF file can contain a number of distinct indexes. Each index is identified by the type of index and the stream number. No ASF index object can contain more than one index for a particular combination of stream number and index type.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/dc38a060-36e4-458e-829e-2770387fc484">IMFASFIndexer::GetIndexStatus</a>



<a href="https://msdn.microsoft.com/bad10893-07af-4b46-bab1-2878553813b5">IMFASFIndexer::SetIndexStatus</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

