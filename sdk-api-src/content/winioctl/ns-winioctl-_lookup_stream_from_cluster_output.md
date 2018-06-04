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

# _LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure


## -description


Received as output from the <a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control code.


## -struct-fields




### -field Offset

Offset from the beginning of this structure to the first entry returned.  If no entries are returned, this value is zero.


### -field NumberOfMatches

Number of matches to the input criteria.  Note that more matches may be found than entries returned if the buffer provided is not large enough.


### -field BufferSizeRequired

Minimum size of the buffer, in bytes, which would be needed to contain all matching entries to the input criteria.


## -see-also




<a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

