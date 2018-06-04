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

# linequeueentry_tag structure


## -description


The 
<b>LINEQUEUEENTRY</b> structure provides the information for a single queue entry. The 
<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a> structure can contain an array of 
<b>LINEQUEUEENTRY</b> structures. This structure requires TAPI 3.0 version negotiation.


## -struct-fields




### -field dwQueueID

Unique identifier for a queue. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwNameSize

Size of the queue name string including the <b>null</b> terminator, in bytes.


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the queue. The size of the string is specified by <b>dwNameSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>



<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a>
 

 

