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

# PDD_GETAVAILDRIVERMEMORY callback function


## -description


The <b>DdGetAvailDriverMemory</b> callback function queries the amount of free memory in the driver-managed memory heap.


## -parameters




### -param Arg1








#### - lpGetAvailDriverMemory

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551532">DD_GETAVAILDRIVERMEMORYDATA</a> structure that contains the information required to perform the query.


## -returns



<b>DdGetAvailDriverMemory</b> returns one of the following callback codes:




## -remarks



This function does not need to be implemented if the memory will be managed by DirectDraw.

<b>DdGetAvailDriverMemory</b> determines how much free memory is in the driver's private heaps for the specified surface type. The driver should check the surface capabilities specified in the <b>DDSCaps</b> member of the following structure against the heaps it is maintaining internally, to determine what heap size to query. For example, if DDSCAPS_NONLOCALVIDMEM is set, the driver should return only contributions from the AGP heaps.

The driver indicates its support of <b>DdGetAvailDriverMemory</b> by implementing a response to GUID_MiscellaneousCallbacks in <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551532">DD_GETAVAILDRIVERMEMORYDATA</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

