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

# linecalllist_tag structure


## -description


The 
<b>LINECALLLIST</b> structure describes a list of call handles. A structure of this type is returned by the 
<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a> and 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a> functions.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwCallsNumEntries

Number of handles in the <i>hCalls</i> array.


### -field dwCallsSize

Size of the array of call handles, in bytes.


### -field dwCallsOffset

Offset from the beginning of the structure to the variably sized array of <b>HCALL</b> handles. The size of the array is specified by <b>dwCallsSize</b>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a>



<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a>
 

 

