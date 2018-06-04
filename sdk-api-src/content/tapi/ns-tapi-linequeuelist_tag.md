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

# linequeuelist_tag structure


## -description


The 
<b>LINEQUEUELIST</b> structure describes a list of queues. This structure can contain an array of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structures. The 
<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a> function returns the 
<b>LINEQUEUELIST</b> structure. 
<b>LINEQUEUELIST</b> requires TAPI 3.0 version negotiation.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structures that appear in the list array. The value is zero if no queue is available.


### -field dwListSize

Size of the agent information array, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structure that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEQUEUEENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a>



<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a>
 

 

