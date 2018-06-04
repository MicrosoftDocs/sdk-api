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

# GlobalMemoryStatus function


## -description


<p class="CCE_Message">[<b>GlobalMemoryStatus</b> can return incorrect information. Use the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function instead.]

Retrieves information about the system's current usage of both physical and virtual memory.


## -parameters




### -param lpBuffer [out]

A pointer to a 
<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a> structure. The 
<b>GlobalMemoryStatus</b> function stores information about current memory availability into this structure.


## -returns



This function does not return a value.




## -remarks



On computers with more than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function can return incorrect information, reporting a value of –1 to indicate an overflow. For this reason, applications should use the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function instead.

On Intel x86 computers with more than 2 GB and less than 4 GB of memory, the 
<b>GlobalMemoryStatus</b> function will always return 2 GB in the <b>dwTotalPhys</b> member of the 
<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a> structure. Similarly, if the total available memory is between 2 and 4 GB, the <b>dwAvailPhys</b> member of the 
<b>MEMORYSTATUS</b> structure will be rounded down to 2 GB. If the executable is linked using the <b>/LARGEADDRESSAWARE</b> linker option, then the 
<b>GlobalMemoryStatus</b> function will return the correct amount of physical memory in both members.

The information returned by the 
<b>GlobalMemoryStatus</b> function is volatile. There is no guarantee that two sequential calls to this function will return the same information.




## -see-also




<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a>



<a href="https://msdn.microsoft.com/7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c">MEMORYSTATUS</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>



<a href="https://msdn.microsoft.com/5e8fca7a-b85f-4bbd-80c1-e580a815fdce">Virtual Address Space and Physical Storage</a>
 

 

